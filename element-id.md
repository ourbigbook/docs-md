# Element ID

↑ **Parent:** [OurBigBook Markup concepts](ourbigbook-markup-concepts.md)

In general usages of a [macro](macro.md) produces an element, and every element has an ID.

IDs must be unique, and they are used as the target of [internal links](internal-link.md).

E.g. due to [Section "Automatic ID from title"](automatic-id-from-title.md), the elements:
```
= Animal

== Big dog

I like <big dogs>.
```
would have IDs respectively:
- `animal`
- `big-dog`

Such IDs are almost always rendered as HTML IDs as something like:
```
<h1 id="animal">
<h2 id="big-dog">
```
and can therefore be linked to in a page with the corresponding fragment:
```
animal.html#big-dog
```

**Table of contents**

- [Reserved IDs](reserved-ids.md)

## ↑ Ancestors (3)

1. [OurBigBook Markup concepts](ourbigbook-markup-concepts.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Automatic ID from title](automatic-id-from-title.md)
- [OurBigBook Web with JavaScript disabled](ourbigbook-web-with-javascript-disabled.md)
- [Visual Studio Code documentation](visual-studio-code-documentation.md)
