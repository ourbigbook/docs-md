<h1 id="web-force-id-extraction"><code>--web-force-id-extraction</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Force [ID extraction](id-extraction.md) on [`-W`, `--web`](web.md), even if article content is unchanged.

This can populate newly introduced IDs or reference types on existing articles. To do this directly from sources already stored on the server, use [web/bin/rerender-articles.js](-/file/web/bin/rerender-articles.js.md) with `--extract-ids`, optionally filtering with `--media` or `--source-pattern`.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`--web-force`](web-force.md)
- [`--web-start-id`](web-start-id.md)
