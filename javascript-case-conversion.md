# JavaScript case conversion

↑ **Parent:** [OurBigBook Markup concepts](ourbigbook-markup-concepts.md)

Some parts of OurBigBook use "JavaScript case conversion".

This means that the conversion is done as if by the `toLowerCase`/`toUpperCase` functions.

The most important fact about those functions is that they do convert non-ASCII Unicode capitalization, e.g. between `É` and `é`:
- [https://stackoverflow.com/questions/3590833/does-javascript-string-tolowercase-follow-unicode-standards-in-case-conversion](https://stackoverflow.com/questions/3590833/does-javascript-string-tolowercase-follow-unicode-standards-in-case-conversion)
- [https://stackoverflow.com/questions/929079/unicode-lowercase-characters](https://stackoverflow.com/questions/929079/unicode-lowercase-characters)

These conversions are also specified in the Unicode standard.

## ↑ Ancestors (3)

1. [OurBigBook Markup concepts](ourbigbook-markup-concepts.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Automatic ID from title](automatic-id-from-title.md)
- [Internal link title inflection](internal-link-title-inflection.md)
- [OurBigBook Web restrictions compared to CLI](ourbigbook-web-restrictions-compared-to-cli.md)
