# Include

↑ **Parent:** [Macro](macro.md)

The `\Include` macro allows including an external OurBigBook headers under the current header.

It exists to allow optional single page HTML output while still retaining the ability to:
- split up large input files into multiple files to make renders faster during document development
- suggest an optional custom output split with one HTML output per OurBigBook input, in order to avoid extremely large HTML pages which could be slow to load

`\Include` takes one mandatory argument: the ID of the section to be included, much like [internal links](internal-link.md).

There is however one restriction: only [the toplevel headers](the-toplevel-header.md) can be pointed to. This restriction allows us to easily find the included file in the filesystem, and dispenses the need to do a first `./ourbigbook` run to generate the [ID database](cross-file-internal-link-internals.md). This works because [the ID of the first header is derived from the filename](the-id-of-the-first-header-is-derived-from-the-filename.md).

Headers of the included document are automatically shifted to match the level of the child of the level where they are being included.

If [`--embed-includes`](embed-includes.md) is given, the external document is rendered embedded into the current document directly, essentially as if the source had been copy pasted (except for small corrections such as the header offsets).

Otherwise, the following effects happen:
- The headers of the included tree appear in the [table of contents](table-of-contents.md) of the document as links to the corresponding external files.

  This is implemented simply by reading a previously generated database file much like [cross file internal link internals](cross-file-internal-link-internals.md), which avoids the slowdown of parsing all included files every time.

  As a result, you have to do an initial parse of all files in the project to extract their headers however, just as you would need to do when linking to those headers.
- the include itself renders as a link to the included document
- [`--embed-includes`](embed-includes.md)

Here is an example of inclusion of the files `not-index.bigb` and `not-index-2.bigb`:
```
\Include[not-index]
\Include[not-index-2]
\Include[not-index-with-scope]
```
The above is the recommended and slightly more [shorthand](macro-shorthand-syntax.md) version of:
```
\Include[not-index]

\Include[not-index-2]

\Include[not-index-with-scope]
```
The shorthand version is a bit shorter because the `\Include` magically discards the following newline node that follows it if it just a plaintext node containing exactly a newline. With a double newline, the newline would already have been previously taken out on the lexing stage as part of a paragraph.

[Section "`\Include` example"](include-example.md) shows what those actually render like.

**Table of contents**

- [`\Include` from subdirectories](include-from-subdirectories.md)
- [`\Include` `parent` argument](include-parent-argument.md)
- [`\Include` example](include-example.md)
  - [Not the index](not-index.md)
    - [mymath $a^2$](not-index.md#mymath-a-2)
    - [h2 in not the index](not-index.md#h2-in-not-the-index)
      - [h3 in not the index](not-index.md#h3-in-not-the-index)
    - [Some references back to the index](not-index.md#some-references-back-to-the-index)
    - [Not the index header with scope](not-index.md#not-the-index-header-with-scope)
      - [Not the index header with scope child](not-index.md#not-the-index-header-with-scope/not-the-index-header-with-scope-child)
    - [Not the index header with fixed case](not-index.md#not-the-index-header-with-fixed-case)
      - [Header with scope child](not-index.md#header-with-scope-child)
    - [Not the index another include](not-index.md#not-the-index-another-include)
      - [Included by not the index](included-by-not-index.md)
        - [Included by not the index 2](included-by-not-index.md#included-by-not-the-index-2)
  - [Not the index 2](not-index-2.md)
  - [Not the index with scope](not-index-with-scope.md)
    - [h2](not-index-with-scope.md#h2)
    - [h2 2](not-index-with-scope.md#h2-2)
      - [h3](not-index-with-scope.md#h3)
  - [Subdir](subdir.md)
    - [Included by index](subdir/included-by-index.md)
    - [H2](subdir.md#h2)
    - [Ourbigbook](subdir.md#ourbigbook)
  - [Notindex](subdir/notindex.md)
    - [Notindex h2](subdir/notindex.md#notindex-h2)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (9)

- [`--embed-includes`](embed-includes.md)
- [Features](features.md)
- [`\H` `splitDefault` argument](h-splitdefault-argument.md)
- [`\H` `toplevel` argument](h-toplevel-argument.md)
- [`\Include` `parent` argument](include-parent-argument.md)
- [`--log perf`](log-perf.md)
- [OurBigBook CLI enforces consistent header tree by default](news/ourbigbook-cli-enforces-consistent-header-tree-by-default.md)
- [`Numbered`](ourbigbook-json/h/numbered.md)
- [The ID of the first header is derived from the filename](the-id-of-the-first-header-is-derived-from-the-filename.md)
