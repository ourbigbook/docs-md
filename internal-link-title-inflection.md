# Internal link title inflection

↑ **Parent:** [Internal link](internal-link.md)

In most cases it is generally more convenient to simply use the [`\x` `magic` argument](x-magic-argument.md) through [shorthand internal links](shorthand-internal-link.md) instead of the `c` and `p` arguments as described on the rest of this section, see also: [Section "Inflection vs magic"](inflection-vs-magic.md).

A common usage pattern is that we want to use [header](header.md) titles in [non-full](x-full-argument.md) [internal links](internal-link.md) as the definition of a concept without repeating the title, for example:
```
== Dog

Cute animal.

\x[cats][Cats] are its natural enemies.

== Cats

This is the natural enemy of a \x[dog][dog].

\x[dog][Dogs] are cute, but they are still the enemy.

One example of a cat is \x[felix-the-cat].

=== Felix the Cat

Felix is not really a \x[cats][cat], just a carton character.
```

However, word [inflection](https://en.wikipedia.org/wiki/Inflection) makes it much harder to avoid retyping the definition again.

For example, in the previous example, without any further intelligent behaviour we would be forced to re-type `\x[dog][dog]` instead of the desired `\x[dog]`.

OurBigBook can take care of some inflection cases for you.

For capitalization, both headers and [internal link](internal-link.md) macros have the `c` [boolean argument](boolean-argument.md) which stands for "capitalized":
- for headers, `c` means that the header title has fixed capitalization as given in the title, i.e.
  - if the title has a capital first character, it will always show as a capital, as is the case for most [proper noun](https://en.wikipedia.org/wiki/Proper_noun)
  - if it is lower case, it will also always remain lower case, as is the case for some rare proper nouns, notably [the name of certain companies](https://en.wikipedia.org/wiki/Arm_Holdings)

  This means that for such headers, `c` in the `x` has no effect. Maybe we should give an error in that case. But lazy now, send PR.
- for [internal link](internal-link.md) macros, `c` means that the first letter of the title should be capitalized.

  Using this option is required when you are starting a sentence with a non-proper noun.
Capitalization is handled by a [JavaScript case conversion](javascript-case-conversion.md).

For pluralization, [internal link](internal-link.md) macros have the `p` [boolean argument](boolean-argument.md) which stands for "pluralize":
- if given and true, this automatically pluralizes the last word of the target title by using the [blakeembrey/pluralize](blakeembrey-pluralize.md) library.
- if given and false, automatically singularize
- if not given, don't change the number of elements
If your desired pluralization is any more complex than modifying the last word of the title, you must do it manually however.

With those rules in mind, the previous OurBigBook example can be written with less repetition as:
```
== Dog

Cute animal.

\x[cats]{c} are its natural enemies.

== Cats

This is the natural enemy of a \x[dog].

\x[dog]{p} are cute, but they are still the enemy.

One example of a cat is \x[Felix the Cat].

=== Felix the Cat
{c}

Felix is not really a \x[cats][cat], just a carton character.
```

If plural and capitalization don't handle your common desired inflections, you can also just create custom ones with the [`\H` `synonym` argument](h-synonym-argument.md).

Now for a live example for quick and dirty interactive testing.

**Table of contents**

- [Internal link title inflection example](internal-link-title-inflection-example.md)
  - [Inflection example not-proper](inflection-example-not-proper.md)
  - [Inflection example proper](inflection-example-proper.md)
  - [inflection example not-proper lower](inflection-example-not-proper-lower.md)
  - [inflection example proper lower](inflection-example-proper-lower.md)
  - [Inflection plural examples](inflection-plural-examples.md)
- [blakeembrey/pluralize](blakeembrey-pluralize.md)

## ↑ Ancestors (4)

1. [Internal link](internal-link.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (8)

- [Blakeembrey/pluralize](blakeembrey-pluralize.md)
- [Features](features.md)
- [`\H` `c` argument](h-c-argument.md)
- [Inflection vs magic](inflection-vs-magic.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
- [`\x` `c` argument](x-c-argument.md)
- [`\x` `magic` argument](x-magic-argument.md)
- [`\x` `p` argument](x-p-argument.md)
