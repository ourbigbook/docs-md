# Automatic ID from title

↑ **Parent:** [`\H` `title` argument](h-title-argument.md)

If a [non-toplevel](the-toplevel-header.md) macro has the `title` argument is present but no explicit `id` argument is given, an [Element ID](element-id.md) is created automatically from the `title`, by applying the following transformations:
- do a [`id` output format](id-output-format.md) conversion on the title to remove for example any HTML tags that would be present in the conversion output
- convert all characters to lowercase. This uses [JavaScript case conversion](javascript-case-conversion.md). Note that this does convert non-ASCII characters to lowercase, e.g. `É` to `é`.
- if [`id` `normalize` `latin`](ourbigbook-json/id-normalize-latin.md) is `true` (the default) do [Latin normalization](ourbigbook-json/latin-normalization.md). This converts e.g. `é` to `e`.
- if [`id` `normalize` `punctuation`](ourbigbook-json/id-normalize-punctuation.md) is `true` (the default) do [Punctuation normalization](ourbigbook-json/punctuation-normalization.md). This converts e.g. `+` to `plus`.
- convert consecutive sequences of all non `a-z0-9` ASCII characters to a single hyphen `-`. Note that this leaves non-ASCII characters untouched.
- strip leading or trailing hyphens
Note how those rules leave non-ASCII Unicode characters untouched, except for:
- capitalization changes wher applicable, e.g. `É` to `é`
as capitalization and determining if something "is a letter or not" in those cases can be tricky.

For toplevel headers, see: [the ID of the first header is derived from the filename](the-id-of-the-first-header-is-derived-from-the-filename.md).

So for example, the following automatic IDs would be generated: [Table 2. "Examples of automatically generated IDs"](#table-examples-of-automatically-generated-ids).

<a id="table-examples-of-automatically-generated-ids"></a>
| title | id | latin normalization | punctuation normalization | comments |
| --- | --- | --- | --- | --- |
| My favorite title | my-favorite-title |  |  |  |
| Ciro's markdown is awesome | ciro-s-markdown-is-awesome |  |  | `'` is an ASCII character, but it is not in `a-z0-9`, therefore it gets converted to a hyphen `-` |
| É你 | e你 | true |  | The Latin [acute accented](https://en.wikipedia.org/wiki/Acute_accent) `e`, `É`, is converted to its lower case form `é` as per the [JavaScript case conversion](javascript-case-conversion.md). Then, due to [Latin normalization](ourbigbook-json/latin-normalization.md), `é` is converted to `e`. The Chinese character `你` is left untouched as Chinese characters have no case, and no ASCII analogue. |
| É你 | é你 | false |  | Same as the previous, but `é` is not converted to `e` since [Latin normalization](ourbigbook-json/latin-normalization.md) is turned off. |
| C++ is great | c-plus-plus-is-great |  | true | This is the effect of [Punctuation normalization](ourbigbook-json/punctuation-normalization.md). |
| I _love_ dogs. | i-love-dogs |  |  | `love` is extracted from the italic tags `<i>love</i>` with [`id` output format](id-output-format.md) conversion. |
| β Centauri | beta-centauri |  |  | Our Latin normalization is amazing and knows Greek! |

For [the toplevel header](the-toplevel-header.md), its ID is derived from the basename of the OurBigBook file without extension instead of from the `title` argument.

TODO:
- maybe we should also remove some or all non-ASCII punctuation. All can be done with `\\p{IsPunctuation}`: [https://stackoverflow.com/questions/13925454/check-if-string-is-a-punctuation-character](https://stackoverflow.com/questions/13925454/check-if-string-is-a-punctuation-character) but we need to check that we really want to remove all of them.

## ↑ Ancestors (6)

1. [`\H` `title` argument](h-title-argument.md)
2. [`\H` arguments](h-arguments.md)
3. [Header](header.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (14)

- [`description` argument](description-argument.md)
- [`Disambiguate` argument](disambiguate-argument.md)
- [Element ID](element-id.md)
- [`\H` `file` argument](h-file-argument.md)
- [`\H` `title` argument](h-title-argument.md)
- [`Id` argument](id-argument.md)
- [`Id` output format](id-output-format.md)
- [ID target from title](id-target-from-title.md)
- [Internal link](internal-link.md)
- [`Ourbigbook.json` `id`](ourbigbook-json/id.md)
- [The ID of the first header is derived from the filename](the-id-of-the-first-header-is-derived-from-the-filename.md)
- [`title` argument](title-argument.md)
- [`--title-to-id`](title-to-id.md)
- [`\x` `magic` argument](x-magic-argument.md)
