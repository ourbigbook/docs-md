<h1 id="ourbigbook-json/tocmaxentries"><code>tocMaxEntries</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

Maximum number of entries in each static HTML [table of contents](../table-of-contents.md). Set a non-negative integer; `0` (the default) means unlimited. For example:
```
{
  "tocMaxEntries": 1000
}
```

If the table exceeds this limit, the deepest level is removed in full, repeatedly, until the remaining entries fit. Every retained depth level remains complete across all branches. The first level is always kept, even if it alone exceeds the limit.

For example, if successive levels contain 4, 10, and 20 entries, a limit of 15 keeps the first two levels (14 entries). A limit of 10 keeps only the first level (4 entries), and a limit of 2 still keeps all 4 first-level entries.

The limit is calculated independently for each output page, including [`-S`, `--split-headers`](../split-headers.md) and [includes](../include.md). Only TOC entries are removed; all document sections remain. TOC shortcuts on omitted headings link to the table of contents itself. This setting does not change [OurBigBook Web](../ourbigbook-web.md) tables of contents.

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Table of contents](../table-of-contents.md)
