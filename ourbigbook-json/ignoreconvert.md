<h1 id="ourbigbook-json/ignoreconvert"><code>ignoreConvert</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

Similar to [`ignore`](ignore.md), but only skips conversion of matching files. [`dontIgnoreConvert`](dontignoreconvert.md) overrides these patterns.

Unlike [`ignore`](ignore.md), matching files are still placed under the [`-/raw` directory](../raw-directory.md) and can be publicly viewed.

You almost always want this option over [`ignore`](ignore.md), with files that should not be in the repository being just ignored with your `.gitignore` instead: [Section "Ignore from `.gitignore`"](../ignore-from-gitignore.md).

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [`DontIgnoreConvert`](dontignoreconvert.md)
