# Related projects

↑ **Parent:** [Design goals](design-goals.md)

Static wiki generators: this is perhaps the best way of classifying this project :-)
- [https://github.com/gollum/gollum](https://github.com/gollum/gollum): already has a local server editor! But no WYSIWYG nor live preview. Git integration by default, so when you save on the UI already generates a Git commit. We could achieve that with: [https://github.com/isomorphic-git/isomorphic-git](https://github.com/isomorphic-git/isomorphic-git), would be really nice. Does not appear to have built-in static generation:
  - [https://stackoverflow.com/questions/7210391/have-anyone-use-gollum-site-to-generete-markdown-wikis-and-host-it-on-heroku](https://stackoverflow.com/questions/7210391/have-anyone-use-gollum-site-to-generete-markdown-wikis-and-host-it-on-heroku)
  - [https://github.com/dreverri/gollum-site](https://github.com/dreverri/gollum-site)

  Does not appear to check that any links are correct.
- [https://github.com/wcchin/markypydia](https://github.com/wcchin/markypydia)
- [https://obsidian.md/](https://obsidian.md/) closed source, Markdown with [cross file internal link](cross-file-internal-link.md) + a SaaS. Appears to require payment for any publishing. 28k followers 2021: [https://twitter.com/obsdmd](https://twitter.com/obsdmd). Founders are likely Canadians of Asian descent from Waterloo University: [https://www.linkedin.com/in/lishid/](https://www.linkedin.com/in/lishid/) | [https://www.linkedin.com/in/ericaxu/](https://www.linkedin.com/in/ericaxu/) also working in parallel on [https://dynalist.io/](https://dynalist.io/) 2020 review at: [https://www.youtube.com/watch?v=aK2fOQRNSxc](https://www.youtube.com/watch?v=aK2fOQRNSxc) Has offline editor with side-by-side preview. Compares with [Roam](https://roamresearch.com/) and [Notion](https://roamresearch.com/), but can't find any public publishing on those, seem to be enterprise only things.

Static book generators:
- [https://github.com/rstudio/bookdown](https://github.com/rstudio/bookdown), [https://bookdown.org/](https://bookdown.org/). Very similar feature set to what we want!!! Transpiles to markdown, and then goes through Pandoc: [https://bookdown.org/yihui/bookdown/pandoc.html](https://bookdown.org/yihui/bookdown/pandoc.html), thus will never run on browser without huge translation layers. But does have an obscene amount of output formats however.
- [Hugo](https://gohugo.io/). Pretty good, similar feature set to ours. But Go based, so hard on browser, and adds adhoc features on top of markdown once again
- [https://en.wikipedia.org/wiki/Personal_wiki](https://en.wikipedia.org/wiki/Personal_wiki)
  - [https://github.com/vimwiki/vimwiki](https://github.com/vimwiki/vimwiki)
- [https://github.com/hplgit/doconce](https://github.com/hplgit/doconce)
- [https://www.gwern.net/About#source](https://www.gwern.net/About#source) is pretty interesting, uses [https://github.com/jaspervdj/Hakyll/](https://github.com/jaspervdj/Hakyll/) + some custom stuff.
- [https://github.com/JerrySievert/bookmarkdown](https://github.com/JerrySievert/bookmarkdown)
- [https://www.gitbook.com/](https://www.gitbook.com/)
  - [https://github.com/rust-lang/mdBook](https://github.com/rust-lang/mdBook). Impressive integrated search feature. Like Gitbook but implemented in Rust.
- [https://github.com/facebook/docusaurus](https://github.com/facebook/docusaurus) React + markdown based, written in TypeScript. So how can it be build fast? Gotta benchmark.
- vimdoc: [http://vimdoc.sourceforge.net/](http://vimdoc.sourceforge.net/) They do have perfectly working [internal links](internal-link.md), see any page e.g. [http://vimdoc.sourceforge.net/htmldoc/pattern.html](http://vimdoc.sourceforge.net/htmldoc/pattern.html).
- typst: [https://github.com/typst/typst](https://github.com/typst/typst) An attempt at a LaTeX killer. Has its own typesetting engine, does not simply transpile to LaTeX. Meant to be faster and simpler to write. No HTML output as of writing: [https://github.com/typst/typst/issues/721](https://github.com/typst/typst/issues/721)

Less related but of interest, similar philosophy to what Ciro wants, but no explicitly reusable system:
- [http://www.uprtcl.io/](http://www.uprtcl.io/)
- [https://libretexts.org](https://libretexts.org)
- [https://physics.info/](https://physics.info/)
- [https://hypertextbook.com/](https://hypertextbook.com/)
- [https://tutorial.math.lamar.edu/](https://tutorial.math.lamar.edu/)

## ↑ Ancestors (3)

1. [Design goals](design-goals.md)
2. [OurBigBook Markup and CLI overview](ourbigbook-markup-and-cli-overview.md)
3. [OurBigBook Project](split.md)
