# Make all links of a static website point to another deployment of the website

↑ **Parent:** [OurBigBook CLI](ourbigbook-cli.md)

This section describes how to make all links of one deployment of your [static](p-publish.md) OurBigBook publication to another location. For example, if you have a:

The use case of this is if you are migrating from one domain to another, but you want to keep your old pages around to not break any links, and you also don't want to redirect users across domains.

For example, this happened Ciro felt that [OurBigBook Web](ourbigbook-web.md) had reach enough maturity to be a reasonable reader alternative to the static website and so considered redirecting:
- static [https://cirosantilli.com](https://cirosantilli.com)
- to [OurBigBook Web](ourbigbook-web.md) dynamic the website under [https://ougbook.com/cirosantilli](https://ougbook.com/cirosantilli)

By doing this setup, for example a link in `https://cirosantilli.com` :
```
= Mathematics

<physics>
```
rather than pointing to:
```
https://cirosantilli.com/physics
```
would instead point to;
```
https://ourbigbook.com/cirosantilli/physics
```

To achieve this, you should use the following options
- [`toSplitHeaders`](ourbigbook-json/tosplitheaders.md)
- [`htmlXExtension`](ourbigbook-json/htmlxextension.md)
- [`xPrefix`](ourbigbook-json/xprefix.md)
- [`publishOptions`](ourbigbook-json/publishoptions.md)
as in:
```
"publishOptions": {
  "toSplitHeaders": true,
  "htmlXExtension": false,
  "xPrefix": "https://ourbigbook.com/cirosantilli/"
},
```

## ↑ Ancestors (2)

1. [OurBigBook CLI](ourbigbook-cli.md)
2. [OurBigBook Project](split.md)
