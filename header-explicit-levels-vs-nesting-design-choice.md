# Header explicit levels vs nesting design choice

↑ **Parent:** [`\H` `parent` argument](h-parent-argument.md)

Arguably, the language would be even saner if we did:
```
\H[My h1][

Paragraph.

\H[My h2][]
]
```
rather than having explicit levels as in `\H[1][My h1]` and so on.

But we chose not to do it like most markups available because it leads to too many nesting levels, and hard to determine where you are without tooling.

Ciro later "invented" (?) [`\H` `parent` argument](h-parent-argument.md), which he feels reaches the perfect balance between the advantages of those two options.

## ↑ Ancestors (6)

1. [`\H` `parent` argument](h-parent-argument.md)
2. [`\H` arguments](h-arguments.md)
3. [Header](header.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`\H` `parent` argument](h-parent-argument.md)
