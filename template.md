<h1 id="template"><code>--template</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Select a custom [Liquid template](https://github.com/harttle/liquidjs) file for the output.

If not given, this option defaults to the value of [`template`](ourbigbook-json/template.md), which if not given defaults to `ourbigbook.liquid.html`.

The repository of this documentation for example has a sample `ourbigbook.liquid.html` at: [ourbigbook.liquid.html](ourbigbook.liquid.html).

If no template is present, the default template at one point was:
```
<!doctype html>
<html lang=en>
<head>
<meta charset=utf-8>
<title>{{ title }}</title>
<style>{{ style }}</style>
</head>
<body class="ourbigbook">
{{ body }}
</body>
</html>
```
This will get out of sync sooner or later with the code, but this should still serve as a good base example for this documentation.

The the above example, you can see a few or our predefined [template variables](template-variable.md):
- `title`: the title based on the toplevel header of the page
- `style`: our default stylesheet
- `body`: the main rendered body

We chose Liquid as our template language because it is server-side safe. This allows you to to download the OurBigBook repository of anyone and just compile it yourself without the fear that it will install malware in your computer, see also [Section "`--unsafe-ace`"](unsafe-ace.md).

Also, if we ever some day offer a compilation service, Liquid is designed to prevent arbitrary code execution and infinite loops in templates.

**Table of contents**

- [ourbigbook.liquid.html](ourbigbook-liquid-html.md)
  - [`rel="canonical"`](rel-canonical.md)
- [Template variable](template-variable.md)
  - [`publishTargetIsWebsite`](publishtargetiswebsite.md)

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [CSS](css.md)
- [ourbigbook.liquid.html](ourbigbook-liquid-html.md)
- [Play with the template](play-with-the-template.md)
- [Subdirectory deployment](subdirectory-deployment.md)
