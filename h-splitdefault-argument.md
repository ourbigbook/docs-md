# `\H` `splitDefault` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)  
🏷️ **Tags:** [Boolean argument](boolean-argument.md)

When using [`-S`, `--split-headers`](split-headers.md), [internal links](internal-link.md) always point to non-split pages as mentioned at [internal link targets in split headers](internal-link-targets-in-split-headers.md).

If the `splitDefault` [boolean argument](boolean-argument.md) is given however:
- the split header becomes the default, e.g. `index.html` is now the split one, and `nosplit.html` is the non-split one
- the header it is given for, and all of its descendant headers will use the split header as the default internal cross target, unless the header is already rendered in the current page. This does not propagate across [includes](include.md) however.

For example, consider `index.bigb`:
```
= Toplevel
{splitDefault}

\x[h2][toplevel to h2]

\x[notindex][toplevel to notindex]

\Include[notindex]

== h2
```
and `notindex.bigb`:
```
= Notindex

\x[h2][notindex to h2]

\x[notindex][notindex to notindex h2]

== Notindex h2
```
Then the following links would be generated:
- `index.html`: split version of `index.bigb`, i.e. does not contain `h2`
  - `toplevel to h2`: `h2.html`. Links to the split version of `h2`, since `h2` is also affected by the `splitDefault` of its parent, and therefore links to it use the split version by default
  - `toplevel to notindex`: `notindex.html`. Links to non-split version of `notindex.html` since that header is not `splitDefault`, because `splitDefault` does not propagate across includes
- `nosplit.html` non-split version of `index.bigb`, i.e. contains `h2`
  - `toplevel to h2`: `#h2`, because even though `h2` is `splitDefault`, that header is already present in the current page, so it would be pointless to reload the split one
  - `toplevel to notindex`: `notindex.html`
- `h2.html` split version of `h2` from `index.bigb`
- `notindex.html`: non-split version of `notindex.bigb`
  - `notindex to h2`: `h2.html`, because `h2` is `splitDefault`
  - `notindex to notindex h2`: `#notindex-h2`
- `notindex-split.html`: split version of `notindex.bigb`
  - `notindex to h2`: `h2.html`, because `h2` is `splitDefault`
  - `notindex to notindex h2`: `notindex.html#notindex-h2`, because `notindex-h2` is not `splitDefault`

The major application of this if you like work with a huge `index.bigb` containing thousands of random small topics.

Splitting those into separate source files would be quite laborious, as it would require duplicating IDs on the filename, and setting up [includes](include.md).

However, after this index reaches a certain size, page loads start becoming annoyingly slow, even despite already loading large assets like [images](image.md) video [videos](video.md) only on hover or click: the annoying slowness comes from the loading of the HTML itself before the browser can jump to the ID.

And even worse: this index corresponds to the main index page of the website, which will make what a large number of users will see be that slowness.

Therefore, once this index reaches a certain size, you can add the `splitDefault` attribute to it, to make things smoother for readers.

And if you have a smaller, more self-contained, and highly valuable tutorial such as [https://cirosantilli.com/x86-paging](https://cirosantilli.com/x86-paging), you can just split that into a separate `.bigb` source file.

This way, any links into the smaller tutorial will show the entire page as generally desired.

And any links from the tutorial, back to the main massive index will link back to split versions, leading to fast loads.

This feature was implemented at: [https://github.com/ourbigbook/ourbigbook/issues/131](https://github.com/ourbigbook/ourbigbook/issues/131)

Note that this huge index style is not recommended however. [Ciro Santilli](ciro-santilli.md) used to do it, but moved away from it. The currently recommended approach is to manually create not too large subtrees in each page. This way, readers can easily view several nearby sections without having to load a new page every time.

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (6)

- [Features](features.md)
- [Important command line options](important-command-line-options.md)
- [Internal link targets in split headers](internal-link-targets-in-split-headers.md)
- [`SplitDefault`](ourbigbook-json/h/splitdefault.md)
- [`SplitDefaultNotToplevel`](ourbigbook-json/h/splitdefaultnottoplevel.md)
- [`ToSplitHeaders`](ourbigbook-json/tosplitheaders.md)
