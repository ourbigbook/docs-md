<h1 id="ourbigbook-json/ignore"><code>ignore</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

List of paths relative to the [project toplevel directory](../project-toplevel-directory.md) that [OurBigBook CLI](../ourbigbook-cli.md) will ignore, unless it also has a match in [`dontIgnore`](dontignore.md).

Each entry is a [JavaScript regular expression](../javascript-regular-expression.md), and it must match the entire path from start to end to count.

If a directory is ignored, all its contents are also automatically ignored.

Useful if your project has a large directory that does not contain OurBigBook sources, and you don't want OurBigBook to mess with it.

Only ignores recursive conversions, e.g. given:
```
  "ignore": [
    "web"
  ]
```
doing:
```
ourbigbook .
```
skips that directory, but
```
ourbigbook web/myfile.bigb
```
converts it because it was explicitly requested.

Examples:
- ignore all files with a given extension;
  ```
  "ignore": [
    ".*\\.tmp",
  ]
  ```

  Yes, it is a bit obnoxious to have to escape `.` and the backslash. We should use some proper globbing library like: [https://github.com/isaacs/node-glob](https://github.com/isaacs/node-glob). But on the other hand [ignore from `.gitignore`](../ignore-from-gitignore.md) makes this mostly useless, as `.gitignore` will be used most of the time.

TODO: also ignore during [`-w`, `--watch`](../watch.md).

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (5)

- [Ignored files](../ignored-files.md)
- [`DontIgnore`](dontignore.md)
- [`DontIgnoreConvert`](dontignoreconvert.md)
- [`IgnoreConvert`](ignoreconvert.md)
- [`Media-providers`](media-providers.md)
