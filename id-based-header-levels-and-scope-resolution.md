# ID-based header levels and scope resolution

↑ **Parent:** [`\H` `parent` argument](h-parent-argument.md)

When mixing both [`\H` `parent` argument](h-parent-argument.md) and [scopes](h-scope-argument.md), things get a bit complicated, because when writing or parsing, we have to first determine the parent header before resolving scopes.

As a result, the follow simple rules are used:
- start from the last header of the highest level
- check if the `{parent=XXX}` is a suffix of its ID
- if not, proceed to the next smaller level, and so on, until a suffix is found

Following those rules for example, a file `tmp.bigb`:
```
= h1
{scope}

= h1 1
{parent=h1}
{scope}

= h1 1 1
{parent=h1-1}

= h1 1 2
{parent=h1-1}

= h1 1 3
{parent=h1/h1-1}

= h1 2
{parent=h1}
{scope}

= h1 2 1
{parent=h1-2}
{scope}

= h1 2 1 1
{parent=h1-2/h1-2-1}
```
will lead to the following header tree with [`--log headers`](log-headers.md):
```
= h1  tmp
== h2 1 tmp/h1-1
=== h3 1.1 tmp/h1-1/h1-1-1
=== h3 1.2 tmp/h1-1/h1-1-2
=== h3 1.3 tmp/h1-1/h1-1-3
== h2 2 tmp/h1-2
=== h3 2.1 tmp/h1-2/h1-2-1
==== h4 2.1.1 tmp/h1-2/h1-2-1/h1-2-1-1
```

## ↑ Ancestors (6)

1. [`\H` `parent` argument](h-parent-argument.md)
2. [`\H` arguments](h-arguments.md)
3. [Header](header.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)
