<h1 id="ourbigbook-json/target"><code>target</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3910"></a>
Options applied only for a specific [`--publish-target`](../publish-target.md). Each target object is merged over the normal `ourbigbook.json` configuration before conversion and publishing, so global options remain as defaults.

<a id="ourbigbook-json/_3911"></a>
For example:<a id="ourbigbook-json/_3912"></a>

```
"target": {
  "github-md": {
    "githubMarkdownMaxBytes": 1000000,
    "publishBranch": "master",
    "publishRemoteUrl": "git@github.com:ourbigbook/docs-md.git"
  }
}
```

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (2)

- [`PublishBranch`](publishbranch.md)
- [`--publish-target github-md`](../publish-target-github-md.md)
