<h1 id="ourbigbook-json/dontignore"><code>dontIgnore</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3740"></a>
List of [JavaScript regular expression](../javascript-regular-expression.md). If a file path matches any of them, then override [`ignore`](ignore.md) and don't ignore the path. E.g., if you have several `.scss` examples that you don't want to convert, but you do want to convert the `main.scss` for the website itself:<a id="ourbigbook-json/_3741"></a>

```
"ignore": [
  ".*\\.scss"
]
"dontIgnore": [
  "main.scss"
]
```

<a id="ourbigbook-json/_3742"></a>
Note however that if an upper directory is ignored, then we don't recurse into it, and `dontIgnore` will have no effect.

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (2)

- [`DontIgnoreConvert`](dontignoreconvert.md)
- [`Ignore`](ignore.md)
