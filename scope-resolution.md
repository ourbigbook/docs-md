# `scope` resolution

↑ **Parent:** [`\H` `scope` argument](h-scope-argument.md)

When nested scopes are involved, [internal links](internal-link.md) resolution peels off the scopes one by one trying to find the closes match, e.g. the following works as expected:
```
= h1
{scope}

== h2
{scope}

=== h3
{scope}

\x[h2]
```
Here OurBigBook:
- first tries to loop for an `h1/h2/h3/h2`, since `h1/h2/h3` is the current scope, but that ID does not exist
- so it removes the `h3` from the current scope, and looks for `h1/h2/h2`, which is still not found
- then it removes the `h2`, leading to `h1/h2`, and that one is found, and therefore is taken

## ↑ Ancestors (6)

1. [`\H` `scope` argument](h-scope-argument.md)
2. [`\H` arguments](h-arguments.md)
3. [Header](header.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)
