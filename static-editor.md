# Static editor

↑ **Parent:** [Browser editor with preview](browser-editor-with-preview.md)

The "static editor" is the [Browser editor with preview](browser-editor-with-preview.md).

It can be viewed live at: [https://docs.ourbigbook.com/_obb/dist/editor](https://docs.ourbigbook.com/_obb/dist/editor) and its main source code is located at: [editor.html](editor.html).

The static editor is a browser-only toy/demo with no persistent storage. We call it "static" because it is able to run on a [static website](p-publish.md), as opposed to the more advanced editor present in [OurBigBook Web](ourbigbook-web.md), which interacts fully with a dynamic database. Both static and dynamic editor codebases are highly factored however, which is why they look identical.

That editor can be viewed directly locally with:
```
git clone --recursive https://github.com/ourbigbook/ourbigbook
cd ourbigbook
npm install
npm run build-assets
firefox dist/editor.html
```

You can also speed up the interactive development loop of editor.html with:
```
npm run webpack-dev
```
as usual when dealing with the [`dist` directory](dist-directory.md).

## ↑ Ancestors (4)

1. [Browser editor with preview](browser-editor-with-preview.md)
2. [Editor support](editor-support.md)
3. [Tooling](tooling.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Browser editor with preview](browser-editor-with-preview.md)
- [Web editor](web-editor.md)
