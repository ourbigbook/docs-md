# Tagged metadata section

↑ **Parent:** [Header metadata section](header-metadata-section.md)

Lists sections that are [secondary children](secondary-children.md) of the current section, i.e. tagged under the current section.

The main header tree hierarchy descendants already show under the [table of contents](table-of-contents.md) instead.

E.g. in:
```
= tmp

== Mammal

== Flying

== Animal

=== Bat
{tag=mammal}
{tag=flying}

=== Bee
{tag=flying}

=== Dog
{tag=mammal}
```
the tagged sections for:
- Mammal will contain Bat and Dog
- Flying will contain Bat and Bee

## ↑ Ancestors (5)

1. [Header metadata section](header-metadata-section.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`\H` `child` argument](h-child-argument.md)
- [Secondary children](secondary-children.md)
