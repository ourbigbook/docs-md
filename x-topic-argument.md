# `\x` `topic` argument

↑ **Parent:** [`\x` arguments](x-arguments.md)  
🏷️ **Tags:** [Boolean argument](boolean-argument.md)

If true, then the target of a this link is called a "topic link" and gets treated specially, pointing to an external [OurBigBook Web topic](ourbigbook-web-topics.md) rather than a header defined in the current project.

For example, when rendering a [static website](p-publish.md), a link such as:
```
\x[Albert Einstein]{topic}
```
would produce output similar to:
```
\a[https://ourbigbook.com/go/topic/john-smith][John Smith]
```
e.g.:
```
\x[Albert Einstein]{topic}
```
which renders as:



> [Albert Einstein](https://ourbigbook.com/go/topic/albert-einstein)

This allows static website creators to easily link to topics they might not have already written about which others may have covered.

The [OurBigBook Web](ourbigbook-web.md) instance linked to can be configured with [`host`](ourbigbook-json/web/host.md).

Those links also work on [OurBigBook Web](ourbigbook-web.md) rendering of course, and point to the current Web instance.

**Table of contents**

- [Shorthand topic link](shorthand-topic-link.md)
  - [Shorthand topic links with a single word](shorthand-topic-links-with-a-single-word.md)
- [Topic link pluralization](topic-link-pluralization.md)

## ↑ Ancestors (5)

1. [`\x` arguments](x-arguments.md)
2. [Internal link](internal-link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
