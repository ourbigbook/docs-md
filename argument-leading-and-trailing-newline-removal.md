# Argument leading and trailing newline removal

↑ **Parent:** [Newline removal](newline-removal.md)

If the very first or very last character of an argument is a newline, then that character is ignored if it would be part of a regular plaintext node.

For example:
```
\C[[
a

b
]]
```
generates something like:
```
<pre><code>a

b</code></pre>
```
instead of:
```
<pre><code>
a

b
</code></pre>
```
This is extremely convenient to improve the readability of code blocks and similar constructs.

The newline is however considered if it would be part of some [macro shorthand syntax](macro-shorthand-syntax.md). For example, we can start an [shorthand list](list.md) inside a [quotations](quotation.md) as in:
```
\Q[
* a
* b
]
```
which renders as:



> > 
> > - a
> > - b

where the shorthand list requires a leading newline `\n* ` to work. That newline is not ignored, even though it comes immediately after the `\Q[` opening.

## ↑ Ancestors (5)

1. [Newline removal](newline-removal.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Newline removal](newline-removal.md)
