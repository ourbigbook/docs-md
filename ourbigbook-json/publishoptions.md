<h1 id="ourbigbook-json/publishoptions"><code>publishOptions</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3905"></a>
Options that should be used only on the published output when publishing with the [`--publish` option](../p-publish.md).

<a id="ourbigbook-json/_3906"></a>
These options are merged directly into the options of the [`convert` function](../convert-function.md).

<a id="ourbigbook-json/_3907"></a>
One example usage is to redirect all links of your [static website](../p-publish.md) to your [OurBigBook Web](../ourbigbook-web.md) profile:

<a id="ourbigbook-json/_3908"></a>
```
  "publishOptions": {
    "htmlXExtension": false,
    "ourbigbook_json": {
      "toSplitHeaders": true,
      "xPrefix": "https://ourbigbook.com/cirosantilli/"
    }
  },
```

<a id="ourbigbook-json/_3909"></a>
If given these options override pre-existing options on the published output.

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Make all links of a static website point to another deployment of the website](../make-all-links-of-a-static-website-point-to-another-deployment-of-the-website.md)
