# Local header deletion on web upload

↑ **Parent:** [`-W`, `--web`](web.md)

If you delete a [header](header.md) locally and then do [`-W`, `--web`](web.md) upload, the article is currently not removed from web.

Instead, we simply make its content become empty, and mark it as [unlisted](ourbigbook-web-unlisted-articles.md).

The reason for this is that the article may have metadata created by other users such as [OurBigBook Web discussions](ourbigbook-web-discussions.md), which we don't want to delete remove.

In order to actually remove the header you should follow the procedure from [Section "OurBigBook Web page renaming"](ourbigbook-web-page-renaming.md), which instead first moves all discussions over to a new article before deleting.

**Table of contents**

- [OurBigBook Web unlisted content](ourbigbook-web-unlisted-articles.md)

## ↑ Ancestors (4)

1. [`-W`, `--web`](web.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [OurBigBook Web unlisted content](ourbigbook-web-unlisted-articles.md)
