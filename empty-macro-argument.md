# `empty` macro argument

↑ **Parent:** [Macro argument property](macro-argument-property.md)

An `empty` macro argument must always be empty, or else an error is raised.

The main application of such arguments is to allow macros that normally take no arguments to be immediately followed by text, e.g.:
```
ab\br[]cd
```
which renders as:



> ab  
> cd

## ↑ Ancestors (5)

1. [Macro argument property](macro-argument-property.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Line break](line-break.md)
- [`NotEmpty` macro argument](notempty-macro-argument.md)
