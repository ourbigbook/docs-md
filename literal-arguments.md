# Literal arguments

↑ **Parent:** [Macro argument](macro-argument.md)

Arguments that are opened with more than one square brackets `[` or curly braces `{` are literal arguments.

In literal arguments, OurBigBook is not parsed, and the entire argument is considered as text until a corresponding close with the same number of characters.

Therefore, you cannot have nested content, but it makes it extremely convenient to write [code blocks](code-block.md) or [mathematics](mathematics.md).

For example, a multiline code block with double open and double close square brackets inside can be enclosed in triple square brackets:
```
A literal argument looks like this in OurBigBook:

\C[[
\C[
A multiline

code block.
]
]]

And another paragraph.
```
which renders as:



> A literal argument looks like this in OurBigBook:
> 
> ```
> \C[
> A multiline
> 
> code block.
> ]
> ```
> 
> And another paragraph.

The same works for inline code:
```
The program \c[[puts("]");]] is very complex.
```
which renders as:



> The program `puts("]");` is very complex.

Within literal blocks, only one thing can be escaped with backslashes are:
- leading open square bracket `[`
- trailing close square bracket `]`

The rule is that:
- if the first character of a literal argument is a sequence of backslashes (`\`), and it is followed by another argument open character (e.g. `[`, remove the first `\` and treat the other characters as regular text
- if the last character of a literal argument is a `\`, ignore it and treat the following closing character (e.g. `]`) as regular text

See the following open input/output pairs:
```
\c[[\ b]]
<code>\ b</code>

\c[[\a b]]
<code>\a b</code>

\c[[\[ b]]
<code>[ b</code>

\c[[\\[ b]]
<code>\[ b</code>

\c[[\\\[ b]]
<code>\\[ b</code>
```
and close examples:
```
\c[[a \]]
<code>a \</code>

\c[[a \]]]
<code>a ]</code>

\c[[a \\]]]
<code>a \]</code>
```

## ↑ Ancestors (4)

1. [Macro argument](macro-argument.md)
2. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (6)

- [Code block](code-block.md)
- [Comment](comment.md)
- [Escape characters](escape-characters.md)
- [Line break](line-break.md)
- [Newline removal](newline-removal.md)
- [Shorthand syntax extra arguments](shorthand-syntax-extra-arguments.md)
