# Newline removal

↑ **Parent:** [Macro argument](macro-argument.md)

OurBigBook ignores most single newlines present in your source code. This allows authors to write much more readable [OurBigBook Markup](ourbigbook-markup.md) source.

This removal includes things like:
- [argument newlines between arguments removal](argument-newlines-between-arguments-removal.md)
- when the newline is surrounded by one or two [block macros](block-macro.md), for example:
  ```
  This quote:\Q[My quote]is very cool
  ```

  is the same as:
  ```
  This quote:
  \Q[My quote]
  is very cool
  ```

  because [quotation](quotation.md) is a [block macro](block-macro.md).
- [argument leading and trailing newline removal](argument-leading-and-trailing-newline-removal.md)

The exception is when the newline is placed between two [inline macros](inline-macro.md), where it generates an explicit [line break](line-break.md). This is particularly useful for poetry, for example:
```
Roses are red
Violets are blue
```
which renders as:



> Roses are red  
> Violets are blue

and produces HTML like:
```
Roses are red<br>Violets are blue
```

Double newlines generate [paragraphs](paragraph.md), and triple newlines are forbidden except in [literal arguments](literal-arguments.md).

**Table of contents**

- [Argument leading and trailing newline removal](argument-leading-and-trailing-newline-removal.md)
- [Argument newlines between arguments removal](argument-newlines-between-arguments-removal.md)
- [Document trailing newline removal](document-trailing-newline-removal.md)

## ↑ Ancestors (4)

1. [Macro argument](macro-argument.md)
2. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Line break](line-break.md)
