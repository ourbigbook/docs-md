# `id` argument

↑ **Parent:** [Common argument](common-argument.md)

Explicitly sets the ID of a macro.

In [OurBigBook Markup](ourbigbook-markup.md), every single macro has an ID, which can be either:
- explicit: extracted from some input given by the user, either the [`id` argument](id-argument.md) or the [`title` argument](title-argument.md). Explicit IDs can be referenced in [Internal links](internal-link.md) and must be unique
- implicit: automatically generated numerical ID. Implicit IDs cannot be referenced in [internal links](internal-link.md) and don't need to be unique. Their primary application is generating on hover links next to everything you hover, e.g. arbitrary paragraphs.

The most common way to assign an ID is implicitly with [automatic ID from title](automatic-id-from-title.md) conversion for macros that have a [`title` argument](title-argument.md).

The [`id` argument](id-argument.md) allows to either override the [automatic ID from title](automatic-id-from-title.md), or provide an explicit ID for elements that don't have a [`title` argument](title-argument.md).

## ↑ Ancestors (5)

1. [Common argument](common-argument.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`Id` argument](id-argument.md)
