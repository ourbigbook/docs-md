<h1 id="format-source"><code>--format-source</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Parse and overwrite the local .bigb [OurBigBook Markup](ourbigbook-markup.md) input source files with the recommended code format. E.g.:
```
ourbigbook index.bigb
```
overwrites `index.bigb` with the recommended formatting, and:
```
ourbigbook .
```
does that for every single file in the current directory.

This option uses the [`bigb` output format](bigb-output-format.md).

In order to reach a final stable state, you might need to run the conversion twice. This is not ideal but we don't have the patience to fix it. The reason is that links in image titles may expand twice. This is the usual type of two level recursion that has caused much more serious problems, see e.g. [`\x` within `title` restrictions](x-within-title-restrictions.md). E.g. starting with:
```
<image my big dog>

\Image[image.png]{title=My <big dog>}

= Big dog
```
the first conversion leads to uppercasing inside the image title:
```
<image my big dog>

\Image[image.png]{title=My <big Dog>}

= Big Dog
```
and the second one to uppercasing the reference to the image title:
```
<image my big Dog>

\Image[image.png]{title=My <big Dog>}

= Big Dog
```

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`Bigb` output format](bigb-output-format.md)
- [Features](features.md)
