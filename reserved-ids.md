# Reserved IDs

↑ **Parent:** [Element ID](element-id.md)

IDs that start with an underscore `_` are reserved for OurBigBook usage, and will give an error if you try to use them, in order to prevent ID conflicts.

For example:
- the [table of contents](table-of-contents.md) uses an ID `_toc` the [ID](element-id.md) of the ToC is always fixed to `toc`. If you try to use that for another element, you will get the following error:
- elements without an explicit ID may receive automatically generated IDs of type `_1`, `_2` and so on

If you use a reserved ID, you will get an error mesasge of type:
```
error: tmp.bigb:3:1: IDs that start with "_" are reserved: "_toc"
```

## ↑ Ancestors (4)

1. [Element ID](element-id.md)
2. [OurBigBook Markup concepts](ourbigbook-markup-concepts.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)
