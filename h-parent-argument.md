# `\H` `parent` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)

In addition to the basic way of specifying header levels with an explicit level number as mentioned at [Section "Header"](header.md), OurBigBook also supports a more indirect ID-based mechanism with the `parent` argument of the `\H` element.

We hightly recommend using `parent` for all but the most trivial documents.

For example, the following fixed level syntax:
```
= My h1

== My h2 1

== My h2 2

=== My h3 2 1
```
is equivalent to the following ID-based version:
```
= My h1

= My h2 1
{parent=my-h1}

= My h2 2
{parent=my-h1}

= My h3 2 1
{parent=my-h2-h}
```

The main advantages of this syntax are felt when you have a huge document with [very large header depths](unlimited-header-levels.md). In that case:
- it becomes easy to get levels wrong with so many large level numbers to deal with. It is much harder to get an ID wrong.
- when you want to move headers around to improve organization, things are quite painful without a refactoring tool (which we intend to provide in the [browser editor with preview](browser-editor-with-preview.md)), as you need to fix up the levels of every single header.

  If you are using the ID-based syntax however, you only have to move the chunk of headers, and change the `parent` argument of a single top-level header being moved.

Note that when the `parent=` argument is given, the header level must be `1`, otherwise OurBigBook assumes that something is weird and gives an error. E.g. the following gives an error:
```
= My h1

== My h2
{parent=my-h1}
```
because the second header has level `2` instead of the required `= My h2`.

When [scopes](h-scope-argument.md) are involved, the rules are the same as those of internal reference resolution, including the leading `/` to break out of the scope in case of conflicts.

Like the [`\H` `child` argument](h-child-argument.md), `parent` also performs [ID target from title](id-target-from-title.md) on the argument, allowing you to use the original spaces and capitalization in the target as in:
```
= Flying animal

= Bat
{parent=Flying animal}
```
which is equivalent to:
```
= Flying animal

= Bat
{parent=flying-animal}
```

See also: [Section "Header explicit levels vs nesting design choice"](header-explicit-levels-vs-nesting-design-choice.md) for further rationale.

**Table of contents**

- [ID-based header levels and scope resolution](id-based-header-levels-and-scope-resolution.md)
- [Header explicit levels vs nesting design choice](header-explicit-levels-vs-nesting-design-choice.md)

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (8)

- [Header explicit levels vs nesting design choice](header-explicit-levels-vs-nesting-design-choice.md)
- [ID-based header levels and scope resolution](id-based-header-levels-and-scope-resolution.md)
- [ID target from title](id-target-from-title.md)
- [`\Include` `parent` argument](include-parent-argument.md)
- [`Lint` `h-parent`](ourbigbook-json/lint-h-parent.md)
- [The home article](the-home-article.md)
- [Vim](vim.md)
- [Visual Studio Code documentation](visual-studio-code-documentation.md)
