# Skipping header levels

↑ **Parent:** [Header](header.md)

The very first header of a document can be of any level, although we highly recommend your document to start with a `\H[1]`, and to contain exactly just one `\H[1]`, as this has implications such as:
- `\H[1]` is used for the document title: [HTML document title](html-document-title.md)
- `\H[1]` does not show on the [table of contents](table-of-contents.md)

After the initial header however, you must not skip a header level, e.g. the following would give an error because it skips level 3:
```
= my 1

== my 1

==== my 4
```

## ↑ Ancestors (4)

1. [Header](header.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)
