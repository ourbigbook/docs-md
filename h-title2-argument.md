# `\H` `title2` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)  
🏷️ **Tags:** [`Multiple` argument](multiple-argument.md)

The `title2` argument can be given to any element that has the `title` argument.

Its usage is a bit like the `description=` argument of [images](image.md), allowing you to add some extra content to the header without affecting its ID.

Unlike `description=` however, `title2` shows up on all [`full`](x-full-argument.md) references, including appearances in the [table of contents](table-of-contents.md), which make it more searchable.

Its primary use cases are:
- give acronyms, or other short names names of fuller titles such as mathematical/programming notation

  One primary reason to not use the acronyms as the main section name is to avoid possible ID ambiguities with other acronyms.
- give the header in different languages

For example, given the OurBigBook input:
```
= Toplevel

The Toc follows:

== North Atlantic Treaty Organization
{c}
{title2=NATO}

\x[north-atlantic-treaty-organization]

\x[north-atlantic-treaty-organization]{full}
```
the rendered output looks like:
```
= Toplevel

The ToC follows:

* North Atlantic Treaty Organization (NATO)

== North Atlantic Treaty Organization (NATO)

North Atlantic Treaty Organization

Section 1. "North Atlantic Treaty Organization (NATO)"
```

Related alternatives to `title2` include:
- [`\H` `disambiguate` argument](disambiguate-argument.md) when you do want to affect the ID to remove ambiguities
- [`\H` `synonym` argument](h-synonym-argument.md)

Parenthesis are added automatically around all rendered `title2`.

The `title2` argument has a special meaning when applied to a [header](header.md) with the [`\H` `synonym` argument](h-synonym-argument.md), see [`\H` `title2` argument of a synonym header](h-title2-argument-of-a-synonym-header.md).

**Table of contents**

- [`\H` `title2` argument of a synonym header](h-title2-argument-of-a-synonym-header.md)

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`\H` `synonym` argument](h-synonym-argument.md)
- [`\H` `title2` argument of a synonym header](h-title2-argument-of-a-synonym-header.md)
