<h1 id="ourbigbook-json/prepublish"><code>prepublish</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3894"></a>
Path of a script that gets executed after conversion, and before upload, when running with the [`--publish` option](../p-publish.md).

<a id="ourbigbook-json/_3895"></a>
The script arguments are:<a id="ourbigbook-json/_3896"></a>

<a id="ourbigbook-json/_3897"></a>
- <a id="ourbigbook-json/_3898"></a>
  the publish output directory.

  <a id="ourbigbook-json/_3899"></a>
  That directory is guaranteed to exist when `prepublish` is called.

  <a id="ourbigbook-json/_3900"></a>
  For `git`-based publish targets, all files are almost ready in there, just waiting for a `git add .` that follows `prepublish`.

  <a id="ourbigbook-json/_3901"></a>
  This means that you can use this script to place or remove files from the final publish output.

<a id="ourbigbook-json/_3902"></a>
If the `prepublish` script returns with a non-zero exit value, the publish is aborted.

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (2)

- [Arbitrary code execution](../arbitrary-code-execution.md)
- [`--unsafe-ace`](../unsafe-ace.md)
