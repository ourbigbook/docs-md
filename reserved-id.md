# Reserved ID

↑ **Parent:** [Element ID](element-id.md)

The following IDs are reserved:
- `-`: reserved as a path component anywhere in an ID, in both static and web output. This forbids `-`, `-/child`, `parent/-`, and `parent/-/child`.
- `_out`: forbidden as the first component of an ID, to protect local build output.
- `.git`: forbidden as the first component of an ID, to protect Git metadata.
- `index`: reserved to prevent collisions with the home page's `index.html`. This check also applies to headers inside scopes.

Other uses of hyphens, such as `my-article`, and leading underscores, such as `_toc` and `_1`, are allowed. `_out` and `.git` are allowed in nested IDs such as `parent/_out` and `parent/.git`.

OurBigBook uses the `-/` namespace for generated IDs. For example:
- the [table of contents](table-of-contents.md) uses the fixed ID `-/toc`
- elements without an explicit ID may receive automatically generated IDs of type `-/1`, `-/2` and so on

If you use a reserved ID, you will get an error message such as:
```
error: tmp.bigb:3:1: The ID path component "-" is reserved for website routes: "-/toc"
```

## ↑ Ancestors (4)

1. [Element ID](element-id.md)
2. [OurBigBook Markup concepts](ourbigbook-markup-concepts.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`-/obb` directory](obb-directory.md)
- [OurBigBook Web URL standards: scoped routes](ourbigbook-web-url-standards-scoped-routes.md)
