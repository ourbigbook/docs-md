# Macro shorthand syntax

↑ **Parent:** [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)

Certain commonly used macros have a shorthand macro syntax that do not start with backslash (`\`). It is a form of [syntactic sugar](https://ourbigbook.com/go/topic/syntactic-sugar).

For example, you could write [code blocks](code-block.md) as:
```
I like my code:
\C[[
print("hello world")
]]
```
which renders as:



> I like my code:
> ```
> print("hello world")
> ```

but that is very verbose and annoying to read and write. Therefore, in addition to the [explicit](macro-shorthand-syntax.md) `\C` syntax, most people will prefer the backtick shorthand syntax:
```
I like my code:
``
print("hello world")
``
```
which renders as:



> I like my code:
> ```
> print("hello world")
> ```

Originally, [Ciro wanted to avoid those](design-goals.md), but they just feel too good to avoid.

Every shorthand syntax does however have an equivalent sane syntax.

Our style recommendation is: use the shorthand version which is shorter, unless you have a specific reason to use the sane version.

Shorthand in our context does not mean worse. It just mean "harder for the computer to understand". But it is more important that humans can understand in the first place! It is find to make the computer work a bit more for us when we are able to.

**Table of contents**

- [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
  - [Code and math shorthands](code-and-math-shorthands.md)
  - [Shorthand syntax extra arguments](shorthand-syntax-extra-arguments.md)
  - [Escapes in macro shorthands](escapes-in-macro-shorthands.md)

## ↑ Ancestors (3)

1. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (6)

- [Argument leading and trailing newline removal](argument-leading-and-trailing-newline-removal.md)
- [Code block](code-block.md)
- [Escape characters](escape-characters.md)
- [Macro](macro.md)
- [Mathematics](mathematics.md)
- [Saner](saner.md)
