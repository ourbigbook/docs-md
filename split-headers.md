<h1 id="split-headers"><code>-S</code>, <code>--split-headers</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Split each header into its own separate HTML output file.

This option allows you to keep all headers in a single source file, which is much more convenient than working with a billion separate source files, and let them grow naturally as new information is added, but still be able to get a small output page on the rendered website that contains just the content of the given header. Such split pages:
- load faster on the browser
- get way better Google PageRank for title hits
- allow for full metadata display, e.g.:
  - [Header metadata section](header-metadata-section.md)
  - [Disqus](https://en.wikipedia.org/wiki/Disqus)/[Giscus](https://github.com/giscus/giscus) comments

For example given an input file called `hello.bigb` and containing:
```
= h1

h1 content.

A link to another section: \x[h1-1].

== h1 1

h1-1 content.

== h1 1 1

h1-1-1 content.

== h1 1 2

h1-1-2 content.
```
a conversion command:
```
ourbigbook --split-headers hello.bigb
```
would produce the following output files:
- `hello.html`: contains the entire rendered document as usual.

  Remember that this is called `hello.html` instead of `h1.html` because [the toplevel header ID is automatically derived from its filename](the-toplevel-header.md).

  Each header contains a on-hover link to the single-file split version of the header.
- `hello-split.html`: contains only the contents directly under `= h1`, but not under any of the subheaders, e.g.:
  - `h1 content.` appears in this rendered output
  - `h1-1-1` does not appear in this rendered output

  The `-split` suffix can be customized with the [`\H` `splitSuffix` argument](h-splitsuffix-argument.md) option.  
  The `-split` suffix is appended in order to differentiate the output path from `hello.html`
- `h1-1.html`, `h1-1-1.html`, `h1-1-2.html`: contain only the contents direcly under their headers, analogously to `hello-split.html`, but now we don't need to worry about the input filename and collisiont, and just directly use the ID of each header

`--split-headers` is implied by the [`--publish` option](p-publish.md): the published website will automatically get the split pages. There is no way to turn it off currently. A pull request would be accepted, especially if it offers a [`ourbigbook.json`](ourbigbook-json.md) way to do it. Maybe it would be nice to have a more generalized way of setting any CLI option equivalent from the `ourbigbook.json`, and an option `cli` vs `cli-publish` so that `cli-publish` is publish only. Just lazy for now/not enough pressing use case met.

**Table of contents**

- [Internal link targets in split headers](internal-link-targets-in-split-headers.md)

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (21)

- [`\a` `href` argument](a-href-argument.md)
- [Conversion process overview](conversion-process-overview.md)
- [Features](features.md)
- [`_file` output directory](file-output-directory.md)
- [`\H` `file` argument](h-file-argument.md)
- [`\H` `splitDefault` argument](h-splitdefault-argument.md)
- [`\H` `splitSuffix` argument](h-splitsuffix-argument.md)
- [`\H` `synonym` argument](h-synonym-argument.md)
- [`\H` `toplevel` argument](h-toplevel-argument.md)
- [Horizontal rule](horizontal-rule.md)
- [Important command line options](important-command-line-options.md)
- [Internal link targets in split headers](internal-link-targets-in-split-headers.md)
- [Internal path links are smart](internal-path-links-are-smart.md)
- [JavaScript redirect to split on missing ID](javascript-redirect-to-split-on-missing-id.md)
- [Link to IDs, not URL path](link-to-ids-not-url-path.md)
- [More powerful](more-powerful.md)
- [Motivation](motivation.md)
- [`OutputOutOfTree`](ourbigbook-json/outputoutoftree.md)
- [OurBigBook Web dynamic article tree](ourbigbook-web-dynamic-article-tree.md)
- [`--publish-target github-md`](publish-target-github-md.md)
- [Template variable](template-variable.md)
