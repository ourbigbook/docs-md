<h1 id="web-force-id-extraction"><code>--web-force-id-extraction</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Force [ID extraction](id-extraction.md) on [`-W`, `--web`](web.md), even if article content is unchanged.

The only use case so far for this has been as a hack for incomplete database updates.

The correct approach is instead to actually re-extract server side as part of the migration. We should do this by implementing a `Article.reextract` analogous to `Article.rerender`, and a helper [web/bin/rerender-articles.js](_file/web/bin/rerender-articles.js.md).

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
