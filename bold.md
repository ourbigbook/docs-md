# Bold

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [Inline macro](inline-macro.md)


```
Some \b[bold] text.
```
which renders as:



> Some **bold** text.

The insane shorthand `**bold**` is equivalent to `\b[bold]`. It can contain other inline macros, including `*italic*`. Use `***both***` for bold italics. Delimiters must be on the same line, with no whitespace immediately inside them. Unmatched delimiters remain literal; use `\*` for a literal asterisk. Code, math and literal arguments do not interpret this shorthand. The list marker `* ` keeps its existing meaning.


```
Some **bold** and **bold *italic*** text.
```
which renders as:



> Some **bold** and **bold _italic_** text.

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Italic](italic.md)
