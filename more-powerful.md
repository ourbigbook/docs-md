# More powerful

↑ **Parent:** [Design goals](design-goals.md)

The [high sanity of OurBigBook](saner.md), also makes creating new macro extensions extremely easy and intuitive.

All built-in language features use the exact same API as new extensions, which ensures that the extension API is sane forever.

Markdown is clearly missing many key features such as block attributes and [internal links](internal-link.md), and has no standardized extension mechanism.

The "more powerful than Asciidoctor" part is only partially true, since Asciidoctor is very featureful can do basically anything through extensions.

The difference is mostly that OurBigBook is completely and entirely focused on making amazing scientific books, and so will have key features for that application out-of-the box, notably:
- amazing header/ToC/ID features including proper error reports: never have a internal broken link or duplicate ID again
- [server side pre-rendered maths with KaTeX](mathematics.md): all divs and spans are ready, browser only applies CSS, no JavaScript gets executed
- [publish](publish-your-content.md): we take care of website publishing for you out-of-the-box, no need to integrate into an external project like Jekyll
- [`-S`, `--split-headers`](split-headers.md):
  - [https://github.com/asciidoctor/asciidoctor/issues/626](https://github.com/asciidoctor/asciidoctor/issues/626) feature request
  - [https://github.com/owenh000/asciidoctor-multipage](https://github.com/owenh000/asciidoctor-multipage) third party plugin that does it
and we feel that some of those features have required specialized code that could not be easily implemented as a standalone macro.

Another advantage over Asciidoctor is that the reference implementation of OurBigBook is in JavaScript, and can therefore be used on browser live preview out of the box. Asciidoctor does Transpile to JS with [Opal](https://github.com/opal/opal), but who wants to deal with that layer of complexity?

## ↑ Ancestors (3)

1. [Design goals](design-goals.md)
2. [OurBigBook Markup and CLI overview](ourbigbook-markup-and-cli-overview.md)
3. [OurBigBook Project](split.md)
