# `\x` `child` argument

↑ **Parent:** [`\x` arguments](x-arguments.md)  
🏷️ **Tags:** [Disabled macro argument](disabled-macro-argument.md)

Setting the `child` [boolean argument](boolean-argument.md) on a [internal link](internal-link.md) to a header as in:
```
\x[my-header]{child}
```
makes that header show up on the list of extra parents of the child.

This argument is deprecated in favor of the [`\H` `tag` argument](h-tag-argument.md).

This allows a section to have multiple parents, e.g. to include it into multiple categories. For example:
```
= Animal

== Mammal

=== Bat

=== Cat

== Flying animal

These animals fly:
* \x[bat]{child}

These animals don't fly:
* \x[cat]
```
would render something like:
```
= Animal

== Mammal

=== Bat (Parent section: Mammal)
(Tags: Flying animal)

=== Cat (Parent section: Mammal)

== Flying animal (Parent section: Animal)

These animals fly:
* \x[bat]

These animals don't fly:
* \x[cat]
```
so note how "Bat" has a list of tags including "Flying animal", but Cat does not, due to the `child`.

This property does not affect how the [table of contents](table-of-contents.md) is rendered. We could insert elements sections there multiple times, but it has the downside that browser Ctrl + F searches would hit the same thing multiple times on the table of contents, which might make finding things harder.
```
== My title{id=my-id}

Read this \x[my-id][amazing section].
```

If the second argument, the [`content` argument](content-argument.md), is not present, it expand to the header title, e.g.:
```
== My title{id=my-id}

Read this \x[my-id].
```
is the same as:
```
== My title{id=my-id}

Read this \x[my-id][My title].
```

**Table of contents**

- [Secondary children](secondary-children.md)

## ↑ Ancestors (5)

1. [`\x` arguments](x-arguments.md)
2. [Internal link](internal-link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [Features](features.md)
- [`\H` `child` argument](h-child-argument.md)
- [Secondary children](secondary-children.md)
- [`\x` `parent` argument](x-parent-argument.md)
