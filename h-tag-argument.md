# `\H` `tag` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)  
🏷️ **Tags:** [`Multiple` argument](multiple-argument.md)

The `\H` `tag` argument marks another header as a tag of the current header.

Tags essentially allow you to classify a single header as a child of multiple headers, as opposed to its location in the header tree which is unique.

Sample usage:
```
= Animal

== Mammal

=== Bat
{tag=Flying animal}

=== Cat

== Bird

=== Humming bird
{tag=Flying animal}

== Flying animal
```

So here we see that `Bat` and `Humming bird` have their unique position in the tree under `Mammal` ane `Bird`. But we also wanted them to be somehow classified under `Flying animal`. Tags allow us to do that.

<a id="image-non-toplevel-tagged-headers-demo"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tag/non-toplevel-documentary-arrows.png" alt="" height="650">

**[Figure 24](#image-non-toplevel-tagged-headers-demo). Non-toplevel tagged headers demo**. Visible live at: [https://cirosantilli.com/film#documentary-film](https://cirosantilli.com/film#documentary-film)

<a id="image-ourbigbook-web-tagged-article-list-with-body-demo"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/tagged.png" alt="" height="1081">

**[Figure 25](#image-ourbigbook-web-tagged-article-list-with-body-demo). OurBigBook Web tagged article list with body demo**. On [OurBigBook Web](ourbigbook-web.md), you can also list all articles tagged by an article while also showing the tagged article bodies rather than just their titles. Live URL: [https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics)

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (9)

- [`\H` `child` argument](h-child-argument.md)
- [ID target from title](id-target-from-title.md)
- [`Multiple` argument](multiple-argument.md)
- [`Lint` `h-tag`](ourbigbook-json/lint-h-tag.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
- [Secondary children](secondary-children.md)
- [Visual Studio Code documentation](visual-studio-code-documentation.md)
- [`\x` `child` argument](x-child-argument.md)
- [`\x` `parent` argument](x-parent-argument.md)
