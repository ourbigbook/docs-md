# Important command line options

↑ **Parent:** [OurBigBook CLI quick start](ourbigbook-cli-quick-start.md)

When you run:
```
npx ourbigbook .
```
it converts all files in the current directory separately, e.g.:
- `index.bigb` to `_out/html/index.html`, since `index` is a magic name that we want to show on the root URL
- `not-index.bigb` to `_out/html/not-index.html`, as this one is a regular name unlike `index`
- `main.scss` to `main.css`

If one of the input files starts getting too large, usually the toplevel `index.bigb` in which you dump everything by default like Ciro does, you can speed up development and just compile files individually with either:
```
npx ourbigbook index.bigb
npx ourbigbook not-index.bigb
```
Note however that when those individual files have a [cross file internal link](cross-file-internal-link.md) to something defined in `not-index.bigb`, e.g. via `\x[h2-in-not-the-index]`, then you must have first previously done pass once with:
```
npx ourbigbook .
```
to parse all files and extract all necessary IDs to the [ID database](cross-file-internal-link-internals.md). That would be optimized slightly with the [`--no-render`](no-render.md) command line option:
```
npx ourbigbook --no-render .
```
to only extract the IDs but not render, which speeds things up considerably

When dealing with large files, you might also be interested in the following amazing options:
- [`-S`, `--split-headers`](split-headers.md)
- [`\H` `splitDefault` argument](h-splitdefault-argument.md)

**Table of contents**

- [Produce a standalone HTML file](produce-a-standalone-html-file.md)

## ↑ Ancestors (3)

1. [OurBigBook CLI quick start](ourbigbook-cli-quick-start.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
