# `\x` `full` argument in cross file internal links

↑ **Parent:** [`\x` `full` argument](x-full-argument.md)

For example in the following [cross file internal link](cross-file-internal-link.md):
```
\x[h2-in-not-the-index]{full}.
```
which renders as:



> [Section "h2 in not the index"](h2-in-not-the-index.md).

we get just something like:
```
Section "h2 in not the index"
```
instead of:
```
Section 1.2 "h2 in not the index"
```
This is because the number "Section 1.2" might already have been used in the current page, leading to confusion.

## ↑ Ancestors (6)

1. [`\x` `full` argument](x-full-argument.md)
2. [`\x` arguments](x-arguments.md)
3. [Internal link](internal-link.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Cross file internal link](cross-file-internal-link.md)
