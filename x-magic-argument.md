# `\x` `magic` argument

↑ **Parent:** [`\x` arguments](x-arguments.md)  
🏷️ **Tags:** [Boolean argument](boolean-argument.md)

This argument makes writing many [internal links](internal-link.md) more convenient, and it was notably introduced because it serves as the sane version of [shorthand internal links](shorthand-internal-link.md).

If given e.g. as in:
```
= Internal reference

\x[Internal references]{magic}
```
the link treated magically as follows:
- content capitalization and pluralization are detected from the string, and implicitly set the [`\x` `c` argument](x-c-argument.md) and [`\x` `p` argument](x-p-argument.md). In the example:
  - `{c}` capitalization is set because `Internal references` starts with an upper case character `I`
  - `{p}` pluralization is set because `Internal references` ends in a plural word
  In this simple example, the content therefore will be exactly `Internal references` as in the source. But note that this does not necessarily need to be the case, e.g. if we had done:
  ```
  \x[Internal Reference]{magic}
  ```
  then the content would be:
  ```
  Internal reference
  ```
  without capital `R`, i.e. everything except capitalization and pluralization is ignored. This forgiving way of doing things means that writers don't need to remember the exact ideal capitalization of everything, which is very hard to remember.

  It also means that any more complex elements will be automatically rendered as usual, e.g. if we had:
  ```
  = \i[Internal] reference

  \x[internal reference]{magic}
  ```
  then the output would still contain the `<i>` italic tag.

  If we had a scope as in `\x[my scope/Internal references]`, then each scope part is checked separately. E.g. in this case we would have upper case `Internal references`, even though `my scope` is lowercase, and so `{c}` would be set.
- the ID is calculated as follows:
  - [automatic ID from title](automatic-id-from-title.md) conversion is performed, with you exception: forwards slashs `/` are kept, in order to make [scopes](h-scope-argument.md) work.

    In our case, there aren't any slashes `/`, so it just gives `internal-references`. But if instead we had e.g.: `\x[my scope/internal reference]{magic}`, then we would reach `my-scope/internal-reference` and not `my-scope-internal-reference`.
  - if there is a match to an existing ID use it. `internal-references` in the plural does not match, so go to the next step
  - if the above failed, try singularizing the last word as in the [`\x` `p` argument](x-p-argument.md) with `p=0` before doing [automatic ID from title](automatic-id-from-title.md) conversion. This gives `internal-reference`, which does exist, and so we use that.

There may be some cases where you might still want to use [internal link title inflection](internal-link-title-inflection.md) however, see: [Section "Inflection vs magic"](inflection-vs-magic.md).

**Table of contents**

- [Shorthand magic link](shorthand-magic-link.md)

## ↑ Ancestors (5)

1. [`\x` arguments](x-arguments.md)
2. [Internal link](internal-link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (5)

- [Conversion process overview](conversion-process-overview.md)
- [Inflection vs magic](inflection-vs-magic.md)
- [Internal link title inflection](internal-link-title-inflection.md)
- [Shorthand cross reference](shorthand-cross-reference.md)
- [`\x` `id` output format](x-id-output-format.md)
