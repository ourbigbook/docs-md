# Built-in LaTeX macros

↑ **Parent:** [LaTeX macros](latex-macros.md)

OurBigBook ships with several commonly used math macros enabled by default.

The full list of built-in macros can be seen at: [default.tex](default.tex).

Here's one example of using `\dv` from the [`physics` package](http://mirrors.ibiblio.org/CTAN/macros/latex/contrib/physics/physics.pdf) for derivatives:
```
$$
\dv{x^2}{x} = 2x
$$
```
which renders as:



> $$
> \dv{x^2}{x} = 2x
> $$

Our goal is to collect the most popular macros from the most popular pre-existing LaTeX packages and make them available with this mechanism.

These built-in macros are currently only available on [OurBigBook CLI](ourbigbook-cli.md) and [OurBigBook Web](ourbigbook-web.md), not when using the [JavaScript API](ourbigbook-library.md) directly. We should likely make that possible as well at some point.

In addition to [default.tex](default.tex), the [KaTeX mhchem extension](https://github.com/KaTeX/KaTeX/tree/main/contrib/mhchem) is also enabled to facilitate typesetting of chemical formulae with the `\ce` and `\pu` macros.

## ↑ Ancestors (5)

1. [LaTeX macros](latex-macros.md)
2. [Mathematics](mathematics.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
