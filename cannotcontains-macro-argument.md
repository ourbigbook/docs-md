# `cannotContains` macro argument

↑ **Parent:** [Macro argument property](macro-argument-property.md)

A set of strings. Each one is a macro that this argument cannot contain.

The prototypical use case of this is to prevent nesting of HTML `<a>` elements which is illegal in HTML and doesn't make much sense anyways, e.g.:
```
\a[http://example.com][\a[http://example2.com]]
```

## ↑ Ancestors (5)

1. [Macro argument property](macro-argument-property.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
