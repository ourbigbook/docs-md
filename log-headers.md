<h1 id="log-headers"><code>--log headers</code></h1>

↑ **Parent:** [`--log`](log.md)

This nifty little option outputs to stderr what the header graph looks like!

It is a bit like a [table of contents](table-of-contents.md) in your terminal, for when you need to have a look at the outline of the document to decide where to place a new header, but are not in the mood to open a browser or use the [browser editor with preview](browser-editor-with-preview.md).

Sample output excerpt for this document:
```
= h1  ourbigbook
== h2 1 quick-start
== h2 2 design-goals
=== h3 2.1 saner
=== h3 2.2 more-powerful
== h2 3 paragraphs
== h2 4 links
```

This option can also serve as a debug tool for header tree related features (confession: that was its original motivation!).

TODO

## ↑ Ancestors (4)

1. [`--log`](log.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [ID-based header levels and scope resolution](id-based-header-levels-and-scope-resolution.md)
- [Table of contents](table-of-contents.md)
