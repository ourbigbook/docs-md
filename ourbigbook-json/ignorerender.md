<h1 id="ourbigbook-json/ignorerender"><code>ignoreRender</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3760"></a>
Similar to [`ignore`](ignore.md), but only ignore the files from rendering converesions such as bigb -\> html, scss -\> css.

<a id="ourbigbook-json/_3761"></a>
Unlike [`ignore`](ignore.md), matching files are still placed under the [`_raw` directory](../raw-directory.md) and can be publicly viewed.

<a id="ourbigbook-json/_3762"></a>
You almost always want this option over [`ignore`](ignore.md), with files that should not be in the repository being just ignored with your `.gitignore` instead: [Section "Ignore from `.gitignore`"](../ignore-from-gitignore.md).

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [`DontIgnoreConvert`](dontignoreconvert.md)
