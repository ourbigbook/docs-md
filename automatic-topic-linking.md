# Automatic topic linking

↑ **Parent:** [OurBigBook Web topics](ourbigbook-web-topics.md)

[OurBigBook Web](ourbigbook-web.md) can automatically create links to topics from regular plaintext. For example, if the following topics exist:
- `/go/topic/quantum-mechanics`
- `/go/topic/mathematicsl-physics`
then writing:

> I like mathematical physics and quantum mechanics.

will automatically be converted to something like:
```
I like <a href="/go/topic/mathematical-physics">mathematical physics</a> <a href="/go/topic/quantum-mechanics">quantum mechanics</a>.
```
This reduces the burden on writers of having to manually create topic links themselves.

This conversion currently has the following limitations:
- because it would lead to too many false postives and be too distracting, auto-generated links currently just have the exact same color as regular text, and users only notice them when mouse hovering
- for performance reasons, only topics with a given maximum number of words are considered. The maximum length is configurable by the [OurBigBook Web admin](ourbigbook-web-admin.md) under [site settings](site-settings-page.md) via the `automaticTopicLinksMaxWords`, and currently defaults to 3. Setting it to 0 turns off the automatic link generation

Topic autolinking becomes especially interesting with auto-generated data to populate a large number of topics, as was done with the [wikibot](wikipedia-bot.md) on [OurBigBook.com](ourbigbook-com.md).

This feature is available only on [OurBigBook Web](ourbigbook-web.md). While it would be possible to implement it for [static website](p-publish.md) generation, it would require downloading information from the server which we don't currently want to implement.

Related:
- [https://github.com/ourbigbook/ourbigbook/issues/356](https://github.com/ourbigbook/ourbigbook/issues/356)

<a id="image-automatic-topic-linking-demo"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/topics/automatic-link.png" alt="" height="1181">

**[Figure 56](#image-automatic-topic-linking-demo). Automatic topic linking demo**. [Source](https://ourbigbook.com/cirosantilli/things-that-i-like).

## ↑ Ancestors (4)

1. [OurBigBook Web topics](ourbigbook-web-topics.md)
2. [OurBigBook Web user manual](ourbigbook-web-user-manual.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Automatic topic linking](automatic-topic-linking.md)
