# `dist` directory

↑ **Parent:** [Generated files](generated-files.md)

`dist/` contains fully embedded packaged versions that work on browsers as per common JavaScript package naming convention. All the following files are generated with Webpack with:
```
npm run webpack
```
which is called from `npm run build-assets`.

When publishing with [OurBigBook CLI](ourbigbook-cli.md), `dist` is placed under the [`_obb` directory](obb-directory.md).

The files in that directory are:
- `dist/ourbigbook.js`: OurBigBook [JavaScript API](ourbigbook-library.md) converter for browser usage. The source entry point for it is located at [index.js](index.js). Contains the code of every single dependency used from `node_modules` used by `index.js`. This is notably used for the live-preview of a [browser editor with preview](browser-editor-with-preview.md).
- `dist/ourbigbook_runtime.js`: similar `dist/ourbigbook.js`, but contains the converted output of [ourbigbook_runtime.js](ourbigbook_runtime.js). You should include this in every OurBigBook HTML output.
- `dist/ourbigbook.css`: minimized CSS needed to view OurBigBook output as intended. Embeds all OurBigBook CSS dependencies, notably the KaTeX CSS without which [mathematics](mathematics.md) displays as garbage. The Sass entry point for it is: [ourbigbook.scss](ourbigbook.scss).
- `dist/editor_css.css`: the CSS of the editor, rendered from [editor.scss](editor.scss).

To develop these files, you absolutely want to use:
```
npm run webpack-dev
```
This runs Webpack in development mode, which has two huge advantages:
- almost instantaneous compilation, as opposed to the unbearable 5 seconds+ of an optimized build
- source maps are enabled, so you can see the fully: [https://blog.jakoblind.no/debug-webpack-app-browser/](https://blog.jakoblind.no/debug-webpack-app-browser/)
`npm run webpack-dev` also enables watch mode, so it keeps running until you turn it off.

This setup also works seamlessly when [developing OurBigBook Web](ourbigbook-web-development.md), just let the watch process run in a separate terminal.

## ↑ Ancestors (4)

1. [Generated files](generated-files.md)
2. [Overview of files in this repository](overview-of-files-in-this-repository.md)
3. [Developing OurBigBook](developing-ourbigbook.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`_obb` directory](obb-directory.md)
- [Static editor](static-editor.md)
