# Inline user-defined LaTeX macros

↑ **Parent:** [User-defined LaTeX macros](user-defined-latex-macros.md)

Besides using [`ourbigbook.tex`](ourbigbook-tex.md), you can also define your own math macros directly in the source code.

This is generally fragile however because it doesn't work:
- across [headers](header.md) on [OurBigBook Web](ourbigbook-web.md)
- across different source files on [OurBigBook CLI](ourbigbook-cli.md). That can be worked around with [`ourbigbook.tex`](ourbigbook-tex.md) on CLI, but [`ourbigbook.tex`](ourbigbook-tex.md) does not work on Web either.

If you still want to do it for some reason, first create an invisible block (with `{show=0}`) defining with a `\newcommand` definition:
```
$$
\newcommand{\foo}[0]{bar}
$${show=0}
```
which renders as:



> $$
> \newcommand{\foo}[0]{bar}
> $$

We make it invisible because this block only contains KaTeX definitions, and should not render to anything.

Then the second math block uses those definitions:
```
$$
\foo
$$
```
which renders as:



> $$
> \foo
> $$

Analogously with `\def`, definition:
```
$$
\gdef\foogdef{bar}
$${show=0}
```
which renders as:



> $$
> \gdef\foogdef{bar}
> $$

and the second block using it:
```
$$
\foogdef
$$
```
which renders as:



> $$
> \foogdef
> $$

And just to test that `{show=1}` actually shows, although it is useless, and that `{show=0}` skips incrementing the equation count:
```
$$1 + 1$${show=1}
$$2 + 2$${show=0}
$$3 + 3$${show=1}
```
which renders as:



> 
> 
> $$
> 1 + 1
> $$
> 
> 
> 
> $$
> 2 + 2
> $$
> 
> 
> 
> $$
> 3 + 3
> $$

## ↑ Ancestors (6)

1. [User-defined LaTeX macros](user-defined-latex-macros.md)
2. [LaTeX macros](latex-macros.md)
3. [Mathematics](mathematics.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)
