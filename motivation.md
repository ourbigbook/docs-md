# Motivation

↑ **Parent:** [Design goals](design-goals.md)

[Ciro Santilli](ciro-santilli.md) developed OurBigBook to perfectly satisfy his writing style, which is basically "create one humongous document where you document everything you know about a subject so everyone can understand it, and just keep adding to it".

[https://cirosantilli.com](https://cirosantilli.com) is the first major document that he has created in OurBigBook.

He decided to finally create this new system after having repeatedly facing limitations of Asciidoctor which were ignored/wontfixed upstream, because Ciro's  writing style is not as common/targeted by Asciidoctor.

Following large documents Ciro worked extensively on:
- [https://github.com/cirosantilli/china-dictatorship](https://github.com/cirosantilli/china-dictatorship)
- [https://github.com/cirosantilli/linux-kernel-module-cheat](https://github.com/cirosantilli/linux-kernel-module-cheat)
made the limitations of Asciidoctor clear to Ciro, and were major motivation in this work.

The key limitations have repeatedly annoyed Ciro were:
- cannot go over header level 6, addressed at: [unlimited header levels](unlimited-header-levels.md)
- the need for [`-S`, `--split-headers`](split-headers.md) to avoid one too large HTML output that will never get indexed properly by search engines, and takes a few seconds to load on any browser, which is unacceptable user experience

## ↑ Ancestors (3)

1. [Design goals](design-goals.md)
2. [OurBigBook Markup and CLI overview](ourbigbook-markup-and-cli-overview.md)
3. [OurBigBook Project](split.md)
