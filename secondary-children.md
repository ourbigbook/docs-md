# Secondary children

↑ **Parent:** [`\x` `child` argument](x-child-argument.md)

The term refers to sections that have a parent/child relationship via either of the:
- [`\x` `child` argument](x-child-argument.md)
- [`\x` `parent` argument](x-parent-argument.md)
- [`\H` `child` argument](h-child-argument.md)
- [`\H` `tag` argument](h-tag-argument.md)
rather than via the usual [header](header.md) hierarchy.

Secondary children show up for example on the [tagged metadata section](tagged-metadata-section.md), but not on the [table of contents](table-of-contents.md), which is what the header hierarchy already shows.

Secondary children are normally basically used as "tags": a header such as `Bat` can be a direct child of `Mammal`, and a secondary child of `Flying animal`, or vice versa. Both `Mammal` and `Flying animal` are then basically ancestors. But we have to chose one main ancestor as "the parent", and other secondary ancestors will be seen as tags.

This option first does [ID target from title](id-target-from-title.md) conversion on the argument, so you can e.g. keep any spaces or use capitalization in the title as in:
```
= Animal

== Flying animal
{child=Big bat}

== Big bat
```
TODO the fact that this transformation is done currently makes it impossible to use "non-standard IDs" that contain spaces or uppercase letters. If someone ever wants that, we could maybe add a separate argument that does not do the expansion e.g.:
```
= Animal

== Flying animal
{childId=Big bat}

== Big bat
{id=Big bat}
```
but definitely the most important use case is having easier to type and read source with the standard IDs.

## ↑ Ancestors (6)

1. [`\x` `child` argument](x-child-argument.md)
2. [`\x` arguments](x-arguments.md)
3. [Internal link](internal-link.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Tagged metadata section](tagged-metadata-section.md)
