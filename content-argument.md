# `content` argument

↑ **Parent:** [Pseudo-macro argument property](pseudo-macro-argument-property.md)

The [`content` argument](content-argument.md) of macros contains the "main content" of the macro, i.e. the textual content that will show the most proeminently once the macro is rendered. It is usually, but not always, the first [positional argument](positional-argument.md) of macros. We should probably make it into an official [macro argument property](macro-argument-property.md) at some point.

In most cases, it is quite obvious which argument is the [`content` argument](content-argument.md), e.g.:
- [`\i` macro](italic.md): in `\i[asdf qwer]` then `asdf qwer` is the [`content` argument](content-argument.md)
- [`\a` macro](link.md): in `\a[https://example.com][example website]` then `example website` is the [`content` argument](content-argument.md)

Some macros however don't have a [`content` argument](content-argument.md), especially when they don't show any textual acontent as their primary rendered output, e.g.:
- [`\Image` macro](image.md): this macro has `title` byt not content, e.g. as in: `\Image[flower.jpg]{title=}`, since the primary content is the `Image` rather than any specific text

Philosophically, the [`content` argument](content-argument.md) of a macro is analogous to the `innerHTML` of an HTML tag, as opposed to attributes such as `href=` and so on. The difference is that in [OurBigBook Markup](ourbigbook-markup.md), every macro argument can contain child elements, while in HTML only the `innerHTML`, but not the attributes, can.

## ↑ Ancestors (5)

1. [Pseudo-macro argument property](pseudo-macro-argument-property.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (8)

- [`Auto_parent` macro property](auto-parent.md)
- [`content` argument](content-argument.md)
- [`Disambiguate` argument](disambiguate-argument.md)
- [`Id` output format](id-output-format.md)
- [Positional vs named arguments](positional-vs-named-arguments.md)
- [`Remove_whitespace_children`](remove-whitespace-children.md)
- [The `\Toplevel` implicit macro](toplevel.md)
- [`\x` `child` argument](x-child-argument.md)
