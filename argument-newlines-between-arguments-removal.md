# Argument newlines between arguments removal

↑ **Parent:** [Newline removal](newline-removal.md)

The macro name and the first argument, and any two consecutive arguments, can be optionally separated by exactly one newline character, e.g.:
```
\H
[2]
{scope}
[Design goals]
```
is equivalent to:
```
\H[2]{scope}[Design goals]
```
which is also equivalent to:
```
\H[2]{scope}
[Design goals]
```
This allows to greatly improve the readability of long argument lists by having them one per line.

There is one exception to this however: inside an [shorthand header](header.md), any newline is interpreted as the end of the shorthand header. This is why the following works as expected:
```
== My header 2 `some code`
{id=asdf}
```
and the `id` gets assigned to the header rather than the trailing code element.

## ↑ Ancestors (5)

1. [Newline removal](newline-removal.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Newline removal](newline-removal.md)
