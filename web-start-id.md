<h1 id="web-start-id"><code>--web-start-id</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Start the article upload passes at the selected ID, inclusively, while still replaying any earlier parent and previous-sibling prerequisites needed by the selected suffix. Unrelated articles before the selected ID are skipped. This is useful for resuming a long [`--web-force-id-extraction`](web-force-id-extraction.md) run after a failure, for example:

```
ourbigbook --web --web-force-id-extraction --web-start-id mobius-function
```

The ID must use the local, username-free form and must exist in the upload tree. This option cannot be combined with [`--web-id`](web-id.md). It does not save a checkpoint automatically; use the ID from the first unfinished `web_extract_ids` status line.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Background build](background-build.md)
