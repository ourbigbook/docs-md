<h1 id="ourbigbook-json/ignore"><code>ignore</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3747"></a>
List of paths relative to the [project toplevel directory](../project-toplevel-directory.md) that [OurBigBook CLI](../ourbigbook-cli.md) will ignore, unless it also has a match in [`dontIgnore`](dontignore.md).

<a id="ourbigbook-json/_3748"></a>
Each entry is a [JavaScript regular expression](../javascript-regular-expression.md), and it must match the entire path from start to end to count.

<a id="ourbigbook-json/_3749"></a>
If a directory is ignored, all its contents are also automatically ignored.

<a id="ourbigbook-json/_3750"></a>
Useful if your project has a large directory that does not contain OurBigBook sources, and you don't want OurBigBook to mess with it.

<a id="ourbigbook-json/_3751"></a>
Only ignores recursive conversions, e.g. given:<a id="ourbigbook-json/_3752"></a>

```
  "ignore": [
    "web"
  ]
```
doing:<a id="ourbigbook-json/_3753"></a>

```
ourbigbook .
```
skips that directory, but<a id="ourbigbook-json/_3754"></a>

```
ourbigbook web/myfile.bigb
```
converts it because it was explicitly requested.

<a id="ourbigbook-json/_3755"></a>
Examples:<a id="ourbigbook-json/_3756"></a>

<a id="ourbigbook-json/_3757"></a>
- ignore all files with a given extension;<a id="ourbigbook-json/_3758"></a>

  ```
  "ignore": [
    ".*\\.tmp",
  ]
  ```

  Yes, it is a bit obnoxious to have to escape `.` and the backslash. We should use some proper globbing library like: [https://github.com/isaacs/node-glob](https://github.com/isaacs/node-glob). But on the other hand [ignore from `.gitignore`](../ignore-from-gitignore.md) makes this mostly useless, as `.gitignore` will be used most of the time.

<a id="ourbigbook-json/_3759"></a>
TODO: also ignore during [`-w`, `--watch`](../watch.md).

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (5)

- [Ignored files](../ignored-files.md)
- [`DontIgnore`](dontignore.md)
- [`DontIgnoreConvert`](dontignoreconvert.md)
- [`IgnoreRender`](ignorerender.md)
- [`Media-providers`](media-providers.md)
