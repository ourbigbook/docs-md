<h1 id="remove-whitespace-children"><code>remove_whitespace_children</code></h1>

↑ **Parent:** [Macro argument property](macro-argument-property.md)

In HTML, certain elements such as `<ul>` cannot have any `text` nodes in them, and any whitespace is ignored, see [https://stackoverflow.com/questions/2161337/can-we-use-any-other-tag-inside-ul-along-with-li/60885802#60885802](https://stackoverflow.com/questions/2161337/can-we-use-any-other-tag-inside-ul-along-with-li/60885802#60885802).

A similar concept applies to OurBigBook, e.g.:
```
\Ul[
\L[aa]
\L[bb]
]
```
does not parse as:
```
\Ul[\L[aa]<NEWLINE>\L[bb]<NEWLINE>]
```
but rather as:
```
\Ul[\L[aa]\L[bb]]
```
because the [`content` argument](content-argument.md) of `ul` is marked with `remove_whitespace_children` and automatically removes any whitespace children (such as a newline) as a result.

This also applies to consecutive sequences of [`auto_parent` macro property](auto-parent.md) macros, e.g.:
```
\L[aa]
\L[bb]
```
also does not include the newline between the list items.

The definition of whitespace is the same as the ASCII whitespace definition of HTML5: ` \r\n\f\t`.

## ↑ Ancestors (5)

1. [Macro argument property](macro-argument-property.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Table](table.md)
