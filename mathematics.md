# Mathematics

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [Macro with shorthand syntax](macro-with-shorthand-syntax.md)

Via [KaTeX](https://katex.org/) server side, oh yes!

Inline math is done with the dollar sign (`$`) [macro shorthand syntax](macro-shorthand-syntax.md):
```
My inline $\sqrt{1 + 1}$ is awesome.
```
which renders as:



> My inline $\sqrt{1 + 1}$ is awesome.

and block math is done with two or more dollar signs (`$$`):
```
$$
\sqrt{1 + 1} \\
\sqrt{1 + 1}
$$
```
which renders as:



> $$
> \sqrt{1 + 1} \\
> \sqrt{1 + 1}
> $$

The sane version of inline math is a lower case `m`:
```
My inline \m[[\sqrt{1 + 1}]] is awesome.
```
which renders as:



> My inline $\sqrt{1 + 1}$ is awesome.

and the sane version of block math is with an upper case `M`:
```
\M[[
\sqrt{1 + 1} \\
\sqrt{1 + 1}
]]
```
which renders as:



> $$
> \sqrt{1 + 1} \\
> \sqrt{1 + 1}
> $$

The capital vs lower case theme is also used in other elements, see: [block vs inline macros](block-vs-inline-macros.md).

In the sane syntax, [as with any other argument](escape-characters.md), you have to either escape any closing square brackets `]` with a backslash `\`:
```
My inline \m[1 - \[1 + 1\] = -1] is awesome.
```
which renders as:



> My inline $1 - [1 + 1] = -1$ is awesome.

or with the equivalent double open and close:
```
My inline \m[[1 - [1 + 1] = -1]] is awesome.
```

HTML escaping happens as you would expect, e.g. `<` shows fine in:
```
$$
1 < 2
$$
```
which renders as:



> $$
> 1 < 2
> $$

Equation IDs and titles and linking to equations works identically to [images](image.md), see that section for full details. Here is one equation reference example that links to the following shorthand syntax equation: [Equation 7. "My first shorthand equation"](#equation-my-first-shorthand-equation):
```
$$
\sqrt{1 + 1}
$$
{title=My first shorthand equation}
```
which renders as:



> <a id="equation-my-first-shorthand-equation"></a>
> $$
> \sqrt{1 + 1}
> $$

and the sane equivalent [Equation 8. "My first sane equation"](#equation-my-first-sane-equation):
```
\M{title=My first sane equation}[[
\sqrt{1 + 1}
]]
```
which renders as:



> <a id="equation-my-first-sane-equation"></a>
> $$
> \sqrt{1 + 1}
> $$

Here is a raw one just to test the formatting outside of a `ourbigbook_comment`:

$$
\sqrt{1 + 1}
$$

Here is a very long math equation:

$$
Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello \\
HelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHello \\
Hello
$$

**Table of contents**

- [`\M` argument](m-argument.md)
  - [`\M` `description` argument](m-description-argument.md)
  - [`\M` `title` argument](m-title-argument.md)
- [LaTeX macros](latex-macros.md)
  - [Built-in LaTeX macros](built-in-latex-macros.md)
  - [User-defined LaTeX macros](user-defined-latex-macros.md)
    - [`ourbigbook.tex`](ourbigbook-tex.md)
    - [Inline user-defined LaTeX macros](inline-user-defined-latex-macros.md)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (9)

- [Block vs inline macros](block-vs-inline-macros.md)
- [`Dist` directory](dist-directory.md)
- [`--embed-resources`](embed-resources.md)
- [Escape characters](escape-characters.md)
- [Features](features.md)
- [Literal arguments](literal-arguments.md)
- [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
- [More powerful](more-powerful.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
