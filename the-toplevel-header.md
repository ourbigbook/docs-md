# The toplevel header

↑ **Parent:** [Header](header.md)

The toplevel header of a OurBigBook file is its first header and the one with the lowest level, e.g. in a document with recommended syntax:
```
= Animal

== Dog

=== Bull Terrier

== Cat
```
the header `= Animal` is the toplevel header.

Being the toplevel header gives a header some special handling described in child sections of the section and elsewhere throughout this documentation.

The toplevel header is only defined if the document has only a single header of the highest level. e.g. like the following has only a single `h2`:
```
== My 2

=== My 3 1

=== My 3 2
```

**Table of contents**

- [The toplevel header IDs don't show](the-toplevel-header-ids-don-t-show.md)
- [The ID of the first header is derived from the filename](the-id-of-the-first-header-is-derived-from-the-filename.md)

## ↑ Ancestors (4)

1. [Header](header.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (10)

- [Automatic ID from title](automatic-id-from-title.md)
- [Cross file internal link](cross-file-internal-link.md)
- [`\H` `scope` argument of toplevel headers](h-scope-argument-of-toplevel-headers.md)
- [`\H` `splitSuffix` argument](h-splitsuffix-argument.md)
- [`\H` `toplevel` argument](h-toplevel-argument.md)
- [Include](include.md)
- [Index file](index-file.md)
- [`-S`, `--split-headers`](split-headers.md)
- [Table of contents](table-of-contents.md)
- [Template variable](template-variable.md)
