<h1 id="_file/index.js">index.js</h1>

↑ **Parent:** [`\H` `file` argument demo](../h-file-argument-demo.md)  
🏷️ **Tags:** [Overview of files in this repository](../overview-of-files-in-this-repository.md)

This is a central source file that basically contains all the functionality of the [OurBigBook Library](../ourbigbook-library.md), so basically the [OurBigBook Markup](../ourbigbook-markup.md)-to-[whatever](../output-format.md) (e.g. [HTML](../html-output-format.md)) conversion code, including parsing and rendering.

Things that are not there are things that only use markup conversion, e.g.:
- [OurBigBook CLI](../ourbigbook-cli.md): does conversion from command line
- [OurBigBook Web](../ourbigbook-web.md)

This file must be able to run in the browser, so it must not contain any Node.js specifics.

It exposes the central `convert` function for markup conversion.

You should normally use the packaged `_obb/ourbigbook.js` version of this file when using ourbigbook as an external dependency.

This file is large, and large text files are not previewed, as they would take up too much useless vertical space and disk memory/bandwidth.

## ↑ Ancestors (7)

1. [`\H` `file` argument demo](../h-file-argument-demo.md)
2. [`\H` `file` argument](../h-file-argument.md)
3. [`\H` arguments](../h-arguments.md)
4. [Header](../header.md)
5. [Macro](../macro.md)
6. [OurBigBook Markup](../ourbigbook-markup.md)
7. [OurBigBook Project](../split.md)

## ← Incoming links (2)

- [Adding your first macro](../adding-your-first-macro.md)
- [Overview of files in this repository](../overview-of-files-in-this-repository.md)
