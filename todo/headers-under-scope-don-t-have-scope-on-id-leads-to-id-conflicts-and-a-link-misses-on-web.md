<h1 id="headers-under-scope-don-t-have-scope-on-id-leads-to-id-conflicts-and-a-link-misses-on-web">Headers under scope don't have scope on ID leads to ID conflicts and a link misses on Web</h1>

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Scope](scope.md), [Web](web.md)

E.g. in:
```
= x86

== Sample code

== x86 paging
{scope}

=== Sample code
```

both `Sample code` headers have `id="sample-code"`, which would lead to ID conflicts on the same page.

Also, as a result, the toc link from `x86` intended to go to `x86-paging/sample-code` misses and opens on a separate page.

I don't know how to solve this besides always including scopes on every ID... This does however lead to ugly local IDs on individual pages which is a bit of a shame... oh cruel life.

We could also have two versions of every page, scoped and non scoped, but things likely go exponential when we start dealing with subscope.

This could mean that a lot of toplevel scope removal work will go to the trash! :-( But what can you do, it is the inevitable outcome of dynamic page fetch?

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
