<h1 id="outdir"><code>--outdir &lt;outdir&gt;</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Set a custom output directory for the conversion.

If not given, the [project toplevel directory](project-toplevel-directory.md) is used.

Suppose we have an input file `./test.bigb`. Then:
```
ourbigbook --outdir my_outdir test.bigb
```
places its output at:
```
my_outdir/test.html
```

The same would happen if we instead did a full directory conversion as in:
```
ourbigbook --outdir my_outdir .
```
The output would also be placed in `my_outdir/test.html`.

This option also relocates [the `_out` directory](the-out-directory.md) to the target destination, e.g.:
```
ourbigbook --outdir my_outdir test.bigb
```
would generate:
```
my_outdir/out
```
This means that the source tree remains completely clean, and every output and temporary cache is put strictly under the selected `--outdir`.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`OutputOutOfTree`](ourbigbook-json/outputoutoftree.md)
- [The `_out` directory](the-out-directory.md)
