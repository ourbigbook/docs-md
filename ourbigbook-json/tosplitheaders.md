<h1 id="ourbigbook-json/tosplitheaders"><code>toSplitHeaders</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3936"></a>
Make every [internal link](../internal-link.md) point to the [split header](../split-headers.md) version of the pages of the website. Do this even if those pages don't exist, or if they are not the default target e.g. as per the [`\H` `splitDefault` argument](../h-splitdefault-argument.md).

<a id="ourbigbook-json/_3937"></a>
The initial application of this option was to [Section "Redirect from a static website to a dynamic website"](../make-all-links-of-a-static-website-point-to-another-deployment-of-the-website.md).

<a id="ourbigbook-json/_3938"></a>
If this option is set, then nosplit/split header metadata links are removed, since it was hard to come up with a sensible behaviour to them, and it won't matter on web redirection where every page is nonsplit anyways.

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Make all links of a static website point to another deployment of the website](../make-all-links-of-a-static-website-point-to-another-deployment-of-the-website.md)
