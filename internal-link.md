# Internal link

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [Macro with shorthand syntax](macro-with-shorthand-syntax.md)

Every macro in OurBigBook can have an optional `id` and many also have a reserved `title` property.

When a macro in the document has a `title` argument but no `id` argument given, get an auto-generated ID from the title: [automatic ID from title](automatic-id-from-title.md).

Usually, the most convenient way to write [internal links](internal-link.md) is with the shorthand syntax with delimited angled braces:
```
<internal links> are awesome.
```
which renders as:



> [internal links](internal-link.md) are awesome.

More details at: [shorthand internal link](shorthand-internal-link.md).

The sane equivalent to this is:
```
\x[internal-link]{c}{p} are awesome section.
```
which renders as:



> [Internal links](internal-link.md) are awesome section.

Note how that is more verbose, especially because here we use both the [`\x` `c` argument](x-c-argument.md) and  [`\x` `p` argument](x-p-argument.md) to capitalize and pluraize as desired.

Another sane equivalent would be to add an explicit link body as in:
```
\x[internal-link][Internal link] are awesome.
```
which renders as:



> [Internal link](internal-link.md) are awesome.

**Table of contents**

- [Shorthand internal link](shorthand-internal-link.md)
- [Shorthand cross reference](shorthand-cross-reference.md)
- [Internal link title inflection](internal-link-title-inflection.md)
  - [Internal link title inflection example](internal-link-title-inflection-example.md)
    - [Inflection example not-proper](inflection-example-not-proper.md)
    - [Inflection example proper](inflection-example-proper.md)
    - [inflection example not-proper lower](inflection-example-not-proper-lower.md)
    - [inflection example proper lower](inflection-example-proper-lower.md)
    - [Inflection plural examples](inflection-plural-examples.md)
  - [blakeembrey/pluralize](blakeembrey-pluralize.md)
- [Inflection vs magic](inflection-vs-magic.md)
- [`\x` within `title` restrictions](x-within-title-restrictions.md)
- [Cross file internal link](cross-file-internal-link.md)
  - [Cross file internal link internals](cross-file-internal-link-internals.md)
  - [Link to IDs, not URL path](link-to-ids-not-url-path.md)
  - [Internal link title link removal](internal-link-title-link-removal.md)
- [`\x` arguments](x-arguments.md)
  - [`\x` `c` argument](x-c-argument.md)
  - [`\x` `child` argument](x-child-argument.md)
    - [Secondary children](secondary-children.md)
  - [`\x` `file` argument](x-file-argument.md)
  - [`\x` `full` argument](x-full-argument.md)
    - [`\x` `full` argument in cross file internal links](x-full-argument-in-cross-file-internal-links.md)
  - [`\x` `magic` argument](x-magic-argument.md)
    - [Shorthand magic link](shorthand-magic-link.md)
  - [`\x` `parent` argument](x-parent-argument.md)
  - [`\x` `ref` argument](x-ref-argument.md)
  - [`\x` `topic` argument](x-topic-argument.md)
    - [Shorthand topic link](shorthand-topic-link.md)
      - [Shorthand topic links with a single word](shorthand-topic-links-with-a-single-word.md)
    - [Topic link pluralization](topic-link-pluralization.md)
  - [`\x` `p` argument](x-p-argument.md)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (38)

- [OurBigBook Project](split.md)
- [Boolean argument](boolean-argument.md)
- [Conversion process overview](conversion-process-overview.md)
- [`Disambiguate` argument](disambiguate-argument.md)
- [Element ID](element-id.md)
- [External link](external-link.md)
- [Features](features.md)
- [`\H` `file` argument](h-file-argument.md)
- [`\H` `numbered` argument](h-numbered-argument.md)
- [`\H` `splitDefault` argument](h-splitdefault-argument.md)
- [`\H` `synonym` argument](h-synonym-argument.md)
- [Header](header.md)
- [`Id` argument](id-argument.md)
- [Image](image.md)
- [Image caption](image-caption.md)
- [Image `description` argument](image-description-argument.md)
- [Include](include.md)
- [Internal link](internal-link.md)
- [Internal link targets in split headers](internal-link-targets-in-split-headers.md)
- [Internal link title inflection](internal-link-title-inflection.md)
- [Internal link title link removal](internal-link-title-link-removal.md)
- [Link to IDs, not URL path](link-to-ids-not-url-path.md)
- [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
- [More powerful](more-powerful.md)
- [`--no-html-x-extension`](no-html-x-extension.md)
- [Order of reported errors](order-of-reported-errors.md)
- [`ToSplitHeaders`](ourbigbook-json/tosplitheaders.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
- [OurBigBook Web page renaming](ourbigbook-web-page-renaming.md)
- [Related projects](related-projects.md)
- [`Scope` resolution](scope-resolution.md)
- [Some references back to the index](some-references-back-to-the-index.md)
- [Vim](vim.md)
- [Visual Studio Code documentation](visual-studio-code-documentation.md)
- [`\x` `child` argument](x-child-argument.md)
- [`\x` `full` argument](x-full-argument.md)
- [`\x` `magic` argument](x-magic-argument.md)
- [`\x` within `title` restrictions](x-within-title-restrictions.md)
