# `\Include` `parent` argument

↑ **Parent:** [Include](include.md)

This option is analogous to [`\H` `parent` argument](h-parent-argument.md), but for [includes](include.md).

For example, consider you have:
```
= Animal

== Dog

== Cat

== Bat
```
and now you want to split `Cat` to `cat.bigb`.

If you wrote:
```
= Animal

== Dog

\Include[cat]

== Bat
```
Cat would be a child of Dog, since that is the previous header, which is not what we want.

Instead, we want to write:
```
= Animal

== Dog

\Include[cat]{parent=animal}

== Bat
```
and now Cat will be a child of Animal as desired.

Implemented at: [https://github.com/ourbigbook/ourbigbook/issues/127](https://github.com/ourbigbook/ourbigbook/issues/127)

## ↑ Ancestors (4)

1. [Include](include.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)
