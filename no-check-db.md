<h1 id="no-check-db"><code>--no-check-db</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Skip the database sanity check that is normally done after the [ID extraction](id-extraction.md) step.

This was originally added to speed up, originally added to speed up the [web upload](web.md) development loop, when we knew that there were no errors in the database after a local conversion, and wanted to get to the upload phase faster, but the DB check can take several seconds for a large input.

But it then later also found usage with [Parallel builds](parallel-build.md) followed by a [`--check-db-only`](check-db-only.md).

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
