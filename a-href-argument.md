# `\a` `href` argument

↑ **Parent:** [`\a` argument](a-argument.md)

The link target, e.g. in:
```
\a[http://example.com]
```
`href` equals `http://example.com`.

Important behaviors associated with this property for local links are detailed at [Section "`\a` `external` argument"](a-external-argument.md):
- they are checked for existence in the local filesystem
- they are modified to account for [scopes](h-scope-argument.md) with [`-S`, `--split-headers`](split-headers.md)

## ↑ Ancestors (5)

1. [`\a` argument](a-argument.md)
2. [Link](link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Image `src` argument](image-src-argument.md)
