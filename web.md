<h1 id="web"><code>-W</code>, <code>--web</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)  
🏷️ **Tags:** [Publish your content](publish-your-content.md)

Sync local directory to [OurBigBook Web](ourbigbook-web.md) instead of doing anything else.

To upload the entire repository, run from toplevel:
```
ourbigbook --web
```

To update just all IDs in a single `physics.bigb` source file use:
```
ourbigbook --web physics.bigb
```
This requires that all external IDs that `physics.bigb` might depend on have already been previously uploaded, e.g. with a previous `ourbigbook --web` from toplevel.

The source code is uploaded, and conversion to HTML happens on the server, no conversion is done locally.

Inside a Git repository, uploads use a clean checkout of the current `HEAD` commit, including committed configuration, assets, and pinned submodules. Commit your changes first: uncommitted and untracked files are not uploaded. The checkout is under `_out/publish`, with web output under `_out/publish/_out/web` for a project at the repository root. Configured external local media repositories also use their current commit. Outside Git, uploads continue to use the current files directly, with output under `_out/web`.

Some limitations:
- if there's an error in a later file, the database is still modified by the previous files, i.e. there is no atomicity. A way to improve that would be to upload all files to the server in one go, and let the server convert everything in one transaction. However, this would lead to a very long server action, which would block any other incoming request (I tested, everything is single threaded)

**Table of contents**

- [Local header deletion on web upload](local-header-deletion-on-web-upload.md)
  - [OurBigBook Web unlisted content](ourbigbook-web-unlisted-articles.md)

## 🏷️ Tagged (12)

- [Article and topic ID prefix search](news/article-and-topic-id-prefix-search.md)
- [Article announcement](news/article-announcement.md)
- [Create new articles from table of contents](news/create-new-articles-from-table-of-contents.md)
- [Ourbigbook.com/cirosantilli loads 2x as fast after database optimizations](news/ourbigbook-com-cirosantilli-loads-2x-as-fast-after-database-optimizations.md)
- [Profile picture upload](news/profile-picture-upload.md)
- [Scope ancestors show on toplevel header and page title](news/scope-ancestors-show-on-toplevel-header-and-page-title.md)
- [Signup IP blacklist, VPN detection and account locking](news/signup-ip-blacklist-vpn-detection-and-account-locking.md)
- [Static ToC search](news/static-toc-search.md)
- [Tagged articles and other article lists added to Web](news/tagged-articles-and-other-article-lists-added-to-web.md)
- [Topic ID shows on web editor when creating a new article](news/topic-id-shows-on-web-editor-when-creating-a-new-article.md)
- [Web navigation two level tab cleanup](news/web-navigation-two-level-tab-cleanup.md)
- [Web searches find words inside title on PostgreSQL](news/web-searches-find-words-inside-title-on-postgresql.md)

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (19)

- [Background build](background-build.md)
- [Demo data local file output](demo-data-local-file-output.md)
- [Local header deletion on web upload](local-header-deletion-on-web-upload.md)
- [Disambiguate shows on navigation](news/disambiguate-shows-on-navigation.md)
- [Tagged articles and other article lists added to Web](news/tagged-articles-and-other-article-lists-added-to-web.md)
- [`--no-web-render`](no-web-render.md)
- [OurBigBook CLI](ourbigbook-cli.md)
- [OurBigBook Web unlisted content](ourbigbook-web-unlisted-articles.md)
- [Publish your content](publish-your-content.md)
- [`--web-cancel-build`](web-cancel-build.md)
- [`--web-dry`](web-dry.md)
- [`--web-force`](web-force.md)
- [`--web-force-id-extraction`](web-force-id-extraction.md)
- [`--web-force-render`](web-force-render.md)
- [`--web-id`](web-id.md)
- [`--web-nested-set` (option)](web-nested-set-option.md)
- [`--web-url`](web-url.md)
- [`--web-user`](web-user.md)
- [`--web-watch`](web-watch.md)
