<h1 id="auto-parent"><code>auto_parent</code> macro property</h1>

↑ **Parent:** [OurBigBook Markup concepts](ourbigbook-markup-concepts.md)

Some sequences of macros such as `l` from [lists](list.md) and `tr` from [tables](table.md) automatically generate implicit parents, e.g.:
```
\Ul[
\L[aa]
\L[bb]
]
```
parses exactly like:
```
\L[aa]
\L[bb]
```

The children are always added as arguments of the [`content` argument](content-argument.md) of the implicit parent.

If present, the `auto_parent` macro property determines which auto-parent gets added to those macros.

## ↑ Ancestors (3)

1. [OurBigBook Markup concepts](ourbigbook-markup-concepts.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [List](list.md)
- [`Remove_whitespace_children`](remove-whitespace-children.md)
