# `\H` `synonym` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)

This option is similar to [`\H` `title2` argument](h-title2-argument.md) but it additionally:
- creates a new ID that you can refer to, and renders it with the alternate chosen title
- the rendered ID on [internal links](internal-link.md) is the same as what it is a synonym for
- the synonym header is not rendered at all, including in the [table of contents](table-of-contents.md)
- when using [`-S`, `--split-headers`](split-headers.md), a redirect output file is generated from the synonym to the main ID

Example:
```
= Parent

== GNU Debugger
{c}

= GDB
{c}
{synonym}

I like to say \x[gdb] because it is shorter than \x[gnu-debugger].
```
renders something like:
```
= GNU Debugger

I like to say \a[#gnu-debugger][GDB] because it is shorter than \x[#gnu-debugger][GNU Debugger].
```
Furthermore, if [`-S`, `--split-headers`](split-headers.md) is used, another file is generated:
```
gdb.html
```
which contains a redirection from `gdb.html` to `gnu-debugger.html`.

Implemented at: [https://github.com/ourbigbook/ourbigbook/issues/114](https://github.com/ourbigbook/ourbigbook/issues/114)

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (6)

- [`\H` `synonymNoScope` argument](h-synonymnoscope-argument.md)
- [`\H` `title2` argument](h-title2-argument.md)
- [Internal link title inflection](internal-link-title-inflection.md)
- [`Redirects`](ourbigbook-json/redirects.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
- [The home article](the-home-article.md)
