<h1 id="ourbigbook-tex"><code>ourbigbook.tex</code></h1>

↑ **Parent:** [User-defined LaTeX macros](user-defined-latex-macros.md)

If your project has multiple `.bigb` input files, you can share Mathematics definitions across all files by adding them to the `ourbigbook.tex` file on the toplevel directory.

For example, if `ourbigbook.tex` contains:
```
\newcommand{\foo}[0]{bar}
```
then from any `.bigb` file we in the project can use:
```
$$
\foo
$$
```

Note however that this is not portable to [OurBigBook Web](ourbigbook-web.md) and will likely never be, as we want Web source to be reusable across authors. So the ony way to avoid macro definition conflicts would be to have a namespace system in place, which sounds hard/impossible.

Ideally, you should only use this as a temporary mechanism while you make a pull request to modify the [built-in math macros](built-in-latex-macros.md) :-)

## ↑ Ancestors (6)

1. [User-defined LaTeX macros](user-defined-latex-macros.md)
2. [LaTeX macros](latex-macros.md)
3. [Mathematics](mathematics.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Inline user-defined LaTeX macros](inline-user-defined-latex-macros.md)
