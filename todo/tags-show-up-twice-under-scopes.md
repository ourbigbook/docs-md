# Tags show up twice under scopes

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Scope](scope.md), [Web](web.md)

Happens on CLI, though was first noticed, and most important, on Web due to the all present user prefix.

Was already fully present on the previous deployment but we just completely missed it, e.g.: [https://ourbigbook.com/cirosantilli/physics#physics-education-needs-more-focus-on-understanding-experiments-and-their-history](https://ourbigbook.com/cirosantilli/physics#physics-education-needs-more-focus-on-understanding-experiments-and-their-history)

Minimal CLI example to reproduce:

subdir/asdf.bigb

```
= asdf
```

subdir/qwer.bigb

```
= qwer
{tag=asdf}
```

Then in the rendering of `subdir/qwer.html`, the tag `asdf` appears twice.

The root cause is that scope resolution is finding the same thing twice, one as `subdir/asdf` and then once again with just `asdf` (which is then correctly resolved).

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
