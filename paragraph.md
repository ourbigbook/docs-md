# Paragraph

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [Macro with shorthand syntax](macro-with-shorthand-syntax.md)

The [shorthand](macro-shorthand-syntax.md) syntax is simply to leave a blank line with two consecutive newlines. For example:
```
Paragraph 1.

Paragraph 2.
```
which renders as:



> Paragraph 1.
> 
> Paragraph 2.

Equivalently however, you can use an explicit `\P` macros as well, which is required for example to add properties to a paragraph, e.g.:
```
\P{id=paragraph-1}[Paragraph 1]
\P{id=paragraph-2}[Paragraph 2]
```
which renders as:



> <a id="paragraph-1"></a>
> Paragraph 1
> 
> <a id="paragraph-2"></a>
> Paragraph 2

Paragraphs are created automatically inside [macro argument](macro-argument.md) whenever a double newline appears.

Note that OurBigBook paragraphs render in HTML as `div` with `class="p"` and not as `p`. This means that you can add basically anything inside them, e.g. a list:
```
My favorite list is:
\Ul[
\li[aa]
\li[bb]
]
because it is simple.
```
which renders as a single paragraph.

One major advantage of this, is that when writing documentation, you often want to keep lists or code blocks inside a given paragraph, so that it is easy to reference the entire paragraph with an ID. Think for example of paragraphs in the C++ standard.

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
- [Newline removal](newline-removal.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
- [Saner](saner.md)
