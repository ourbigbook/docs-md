# `\H` `synonymNoScope` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)

The `synonymNoScope` argument works like the [`\H` `synonym` argument](h-synonym-argument.md), except that it ignores any scopes of the synonym target and instead places it at toplevel.

This can be useful if you initially placed a header under a scope, but then decide that some of its descendants would also make sense outside of the scope.

For example consider:

```
= My dog blog

I know a lot about the <history of dog food>.

== Dog food
{scope}

=== History

= History of dog food
{synonymNoScope}
```

In this example, the ID of `History of dog food` is just `history-of-dog-food`, not `dog-food/history-of-dog-food` and therefore we can link to it simply with:
```
<history of dog food>
```
from outside the scope.

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
