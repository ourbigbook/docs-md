<h1 id="rel-canonical"><code>rel="canonical"</code></h1>

↑ **Parent:** [ourbigbook.liquid.html](ourbigbook-liquid-html.md)

The `rel="canonical"` HTML `<head>` tag tells Google the new preferred search result for each page.

You might want to set this up for example if you decide to publish your website both as:
- a [static](p-publish.md) website e.g. under `https://cirosantilli.com`
- on [OurBigBook Web](ourbigbook-web.md) e.g. under `https://ourbigbook.com/cirosantilli`
but you'd like the [OurBigBook Web](ourbigbook-web.md) one to take precedence.

You can set this up by adding something like the following code to the `<head>` element in your [ourbigbook.liquid.html](ourbigbook-liquid-html.md):
```
<link rel="canonical" href="https://ourbigbook.com/cirosantilli/{{ toplevel_id }}">
```
you might also want to do that for all pages except your homepage with:
```
{% unless is_index_article %}<link rel="canonical" href="https://ourbigbook.com/cirosantilli/{{ toplevel_id }}">{% endunless %}
```

## ↑ Ancestors (5)

1. [ourbigbook.liquid.html](ourbigbook-liquid-html.md)
2. [`--template`](template.md)
3. [OurBigBook CLI options](ourbigbook-cli-options.md)
4. [OurBigBook CLI](ourbigbook-cli.md)
5. [OurBigBook Project](split.md)
