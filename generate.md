<h1 id="generate"><code>--generate</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

The project templates are simple ourbigbook project directories that serve as good starting point for new ourbigbook projects.

They also contain useful examples of [OurBigBook Markup](ourbigbook-markup.md) usage to help users get started quickly.

Generate one of the template repositories locally:
- `ourbigbook --generate default`: a good starter template that illustrates many key OurBigBook features
  - [https://github.com/ourbigbook/template](https://github.com/ourbigbook/template)
  - [https://ourbigbook.github.io/template](https://ourbigbook.github.io/template)
- `ourbigbook --generate min`: a minimal template that is still sane
  - [https://github.com/ourbigbook/template-min](https://github.com/ourbigbook/template-min)
  - [https://ourbigbook.github.io/template-min](https://ourbigbook.github.io/template-min)
- `ourbigbook --generate subdir`: a template in which OurBigBook source is located a subdirectory `docs/`:
  - [https://github.com/ourbigbook/template-subdir](https://github.com/ourbigbook/template-subdir)
  - [https://ourbigbook.github.io/template-subdir](https://ourbigbook.github.io/template-subdir)
  This template illustrates that everything works exactly as if OurBigBook source were in the git repository toplevel.

  This is a convenient setup for programming projects that want to use OurBigBook for their documentation without polluting their toplevel.

End users almost never want this, because it means that to have a sane setup you need to:
- install OurBigBook globally with `npm install -g ourbigbook`
- generate the template
- then install OurBigBook locally again with `npm install`
so maybe we should just get rid of that option and just ensure that we can provide an up-to-date working template for the latest relase.

For now we are keeping this as it is useful to automate the updating of templates during the [release procedure](release-procedure.md).

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Play with the template](play-with-the-template.md)
