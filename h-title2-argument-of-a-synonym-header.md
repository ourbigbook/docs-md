# `\H` `title2` argument of a synonym header

↑ **Parent:** [`\H` `title2` argument](h-title2-argument.md)  
🏷️ **Tags:** [Synonym](h-synonym-argument.md)

Unlike [`\H` `title2` argument](h-title2-argument.md), the synonym does not show up by default next to the title. This is because we sometimes want that, and sometimes not. To make the title appear, you can simply add an empty `title2` argument to the synonym header as in:
```
= GNU Debugger
{c}

= GDB
{c}
{synonym}
{title2}

= Quantum computing

= Quantum computer
{synonym}
```
which renders something like:
```
= GNU Debugger (GDB)

= Quantum computing
```
Note how we added the synonym to the title only when it is not just a simple flexion variant, since `Quantum computing (Quantum computer)` would be kind of useless would be kind of useless.

## ↑ Ancestors (6)

1. [`\H` `title2` argument](h-title2-argument.md)
2. [`\H` arguments](h-arguments.md)
3. [Header](header.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`\H` `title2` argument](h-title2-argument.md)
