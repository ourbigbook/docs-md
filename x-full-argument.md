# `\x` `full` argument

↑ **Parent:** [`\x` arguments](x-arguments.md)

To also show the section auto-generated number as in "Section X.Y My title" we add the optional `{full}` [boolean argument](boolean-argument.md) to the [internal link](internal-link.md), for example:
```
\x[x-full-argument]{full}.
```
which renders as:



> [Section "`\x` `full` argument"](x-full-argument.md).

`{full}` is not needed for [internal links](internal-link.md) to most macros besides [headers](header.md), which use `full` by default as seen by the `default_x_style_full` macro property in [`--help-macros`](help-macros.md). This is for example the case for [images](image.md). You can force this to be disabled with `{full=0}`:
```
Compare \x[image-my-test-image]{full=0} vs \x[image-my-test-image]{full=1}.
```
which renders as:



> Compare [The title of my image](image.md#image-my-test-image) vs [Figure 26. "The title of my image"](image.md#image-my-test-image).

**Table of contents**

- [`\x` `full` argument in cross file internal links](x-full-argument-in-cross-file-internal-links.md)

## ↑ Ancestors (5)

1. [`\x` arguments](x-arguments.md)
2. [Internal link](internal-link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (7)

- [Boolean argument](boolean-argument.md)
- [Cross file internal link](cross-file-internal-link.md)
- [`Disambiguate` argument](disambiguate-argument.md)
- [`\H` `numbered` argument](h-numbered-argument.md)
- [`\H` `title2` argument](h-title2-argument.md)
- [Image ID](image-id.md)
- [Internal link title inflection](internal-link-title-inflection.md)
