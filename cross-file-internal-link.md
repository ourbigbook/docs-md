# Cross file internal link

↑ **Parent:** [Internal link](internal-link.md)

<a id="image-cross-file-internal-link"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/x/hilbert-space-arrow.png" alt="" height="571">

**[Figure 44](#image-cross-file-internal-link). Cross file internal link**.

Reference to the first header of another file:
```
\x[not-index]
```
which renders as:



> [not the index](not-index-split.md)

Reference to a non-first header of another file:
```
\x[h2-in-not-the-index]
```
which renders as:



> [h2 in not the index](h2-in-not-the-index.md)

To make toplevel links cleaner, if the target header is the very first element of the other page, then the link does not get a fragment, e.g.: `\x[not-index]` rendered as:
```
<a href="not-index"
```
and not:
```
<a href="not-index#not-index"
```
while `\x[h2-in-not-the-index]` is rendered with the fragment:
```
<a href="not-index#h2-in-not-the-index"
```

Reference to the first header of another file that is a second inclusion:
```
\x[included-by-not-index]
```
which renders as:



> [included by not the index](included-by-not-index-split.md)

Reference to another header of another file, with [`full`](x-full-argument.md):
```
\x[h2-in-not-the-index]{full}.
```
which renders as:



> [Section "h2 in not the index"](h2-in-not-the-index.md).

Note that when `full` is used with references in another file in [multi page mode](embed-includes.md), the number is not rendered as explained at: [Section "`\x` `full` argument in cross file internal links"](x-full-argument-in-cross-file-internal-links.md).

Reference to an image in another file:
```
\x[image-not-index-xi]{full}.
```
which renders as:



> [Figure "Figure in not the index"](h2-in-not-the-index.md#image-not-index-xi).

Reference to an image in another file:
```
\x[image-figure-in-not-the-index-without-explicit-id]{full}.
```
which renders as:



> [Figure "Figure in not the index without explicit id"](h2-in-not-the-index.md#image-figure-in-not-the-index-without-explicit-id).

Remember that the [ID of the toplevel header](the-toplevel-header.md) is automatically derived from its file name, that's why we have to use:
```
\x[not-index]
```
which renders as:



> [not the index](not-index-split.md)

instead of:
```
\x[not-the-index]
```

Reference to a subdirectory:
```
\x[subdir]

\x[subdir/h2]

\x[subdir/notindex]

\x[subdir/notindex-h2]
```
which renders as:



> [subdir](subdir/split.md)
> 
> [h2](subdir/h2.md)
> 
> [notindex](subdir/notindex-split.md)
> 
> [notindex h2](subdir/notindex-h2.md)

Implemented at: [https://github.com/ourbigbook/ourbigbook/issues/116](https://github.com/ourbigbook/ourbigbook/issues/116)

Reference to an internal header of another file: [h2 in not the index](h2-in-not-the-index.md). By default, That header ID gets prefixed by the ID of the top header.

When using [`--embed-includes`](embed-includes.md) mode, the cross file internal links end up pointing to an ID inside the current HTML element, e.g.:
```
<a href="#not-index">
```
rather than:
```
<a href="not-index.html/#not-index">
```
This is why IDs must be unique for elements across all pages.

**Table of contents**

- [Cross file internal link internals](cross-file-internal-link-internals.md)
- [Link to IDs, not URL path](link-to-ids-not-url-path.md)
- [Internal link title link removal](internal-link-title-link-removal.md)

## ↑ Ancestors (4)

1. [Internal link](internal-link.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (12)

- [Cross file internal link](cross-file-internal-link.md)
- [`--embed-includes`](embed-includes.md)
- [Features](features.md)
- [`\H` `c` argument](h-c-argument.md)
- [Important command line options](important-command-line-options.md)
- [Internal link targets in split headers](internal-link-targets-in-split-headers.md)
- [Link to IDs, not URL path](link-to-ids-not-url-path.md)
- [`--log`](log.md)
- [OurBigBook CLI](ourbigbook-cli.md)
- [Related projects](related-projects.md)
- [`-w`, `--watch`](watch.md)
- [`\x` `full` argument in cross file internal links](x-full-argument-in-cross-file-internal-links.md)
