<h1 id="ourbigbook-json/prepublish"><code>prepublish</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

Path of a script that gets executed after conversion, and before upload, when running with the [`--publish` option](../p-publish.md).

The script arguments are:
- the publish output directory.

  That directory is guaranteed to exist when `prepublish` is called.

  For `git`-based publish targets, all files are almost ready in there, just waiting for a `git add .` that follows `prepublish`.

  This means that you can use this script to place or remove files from the final publish output.

If the `prepublish` script returns with a non-zero exit value, the publish is aborted.

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (2)

- [Arbitrary code execution](../arbitrary-code-execution.md)
- [`--unsafe-ace`](../unsafe-ace.md)
