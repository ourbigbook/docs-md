<h1 id="web-no-watch"><code>--web-no-watch</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Exit successfully once the server has accepted the complete upload plan, without waiting for extraction, database checks, rendering, or the final tree rebuild. Implies [`-W`, `--web`](web.md). The server continues processing by itself; exit success confirms submission, not that the build succeeded. Check progress and errors in the Build jobs settings tab or reconnect with [`--web-watch`](web-watch.md). Also works with [`--web-nested-set`](web-nested-set-option.md) to queue a tree rebuild without waiting. Cannot be combined with [`--web-watch`](web-watch.md) or [`--web-individual-upload`](web-individual-upload.md). If an existing build is not replaced, exit without watching or submitting a new build; use [`--web-force`](web-force.md) to replace it non-interactively.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
