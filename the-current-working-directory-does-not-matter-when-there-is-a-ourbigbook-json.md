<h1 id="the-current-working-directory-does-not-matter-when-there-is-a-ourbigbook-json">The current working directory does not matter when there is a <code>ourbigbook.json</code></h1>

↑ **Parent:** [The toplevel index file](the-toplevel-index-file.md)

When the file or directory being converted has an ancestor directory with a `ourbigbook.json` file, then your current working directory does not have any effect on OurBigBook output. For example if we have:
```
/project/ourbigbook.json
/project/index.bigb
/project/subdir/index.bigb
```
then all of the following conversions produce the same output:
- directory conversion:
  - `cd /project && ourbigbook .`
  - `cd / && ourbigbook project`
  - `cd project/subdir && ourbigbook ..`
- file conversion:
  - `cd /project && ourbigbook index.bigb`
  - `cd / && ourbigbook project/index.bigb`
  - `cd project/subdir && ourbigbook ../index.bigb`

When there isn't a `ourbigbook.json`, everything happens as though there were an empty `ourbigbook.json` file in the current working directory. So for example:
- outputs that would be placed relative to inputs are still placed in that place, e.g. `index.bigb -> index.html` always stay together
- outputs that would be placed next to the `ourbigbook.json` are put in the current working directory, e.g. [the `_out` directory](the-out-directory.md)

Internally, the general philosophy is that the JavaScript API in [index.js](index.js) works exclusively with paths relative to the [project toplevel directory](project-toplevel-directory.md). It is then up to callers such as [ourbigbook](ourbigbook) to ensure that filesystem specifics handle the relative paths correctly.

## ↑ Ancestors (5)

1. [The toplevel index file](the-toplevel-index-file.md)
2. [Project toplevel directory](project-toplevel-directory.md)
3. [Index file](index-file.md)
4. [OurBigBook CLI](ourbigbook-cli.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Cross file internal link internals](cross-file-internal-link-internals.md)
- [Project toplevel directory](project-toplevel-directory.md)
