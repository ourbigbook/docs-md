# `multiple` argument

↑ **Parent:** [Macro argument property](macro-argument-property.md)

By default, arguments can be given only once.

However, arguments with the `multiple` [macro argument property](macro-argument-property.md) set to `true` can be given multiple times, and each time the argument is given, the new value is appended to a list containing all the values.

An example is the [`\H` `tag` argument](h-tag-argument.md).

[Internally](internals-api.md), multiple is implemented by creating a new level in the [abstract syntax tree](abstract-syntax-tree.md), and storing each argument separately under a newly generated dummy nodes as in:
```
AstNode: H
  AstArgument: child
    AstNode: Comment
      AstArgument: content
        AstNode: plaintext
        AstNode: x
    AstNode: Comment
      AstArgument: content
        AstNode: plaintext
        AstNode: x
```

## 🏷️ Tagged (3)

- [`\H` `child` argument](h-child-argument.md)
- [`\H` `tag` argument](h-tag-argument.md)
- [`\H` `title2` argument](h-title2-argument.md)

## ↑ Ancestors (5)

1. [Macro argument property](macro-argument-property.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`\H` `child` argument](h-child-argument.md)
