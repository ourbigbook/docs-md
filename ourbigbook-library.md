# OurBigBook Library

↑ **Parent:** [OurBigBook Project](split.md)

The main entry point for the JavaScript API is the `ourbigbook.convert` function.

An example can be seen under [lib_hello.js](lib_hello.js).

Note that while doing a simple conversion is easy, things get harder if you want to take multi-file features in consideration, notably [cross file internal link internals](cross-file-internal-link-internals.md).

This is because these features require interacting with the [ID database](cross-file-internal-link-internals.md), and we don't do that from the default `ourbigbook.convert` API because different deployments will have very different implementations, notably:
- local Node.js run uses SQLite, an implementation can be seen in the [ourbigbook](ourbigbook) file class `SqlDbProvider`
- the in-browser version that runs in the browser editor of the [OurBigBook Web](ourbigbook-web.md) makes API calls to the server

**Table of contents**

- [OurBigBook Library environemnt variable](ourbigbook-library-environemnt-variable.md)
  - [OurBigBook environment variable true](ourbigbook-environment-variable-true.md)
- [`convert` function](convert-function.md)

## ↑ Ancestors (1)

1. [OurBigBook Project](split.md)

## ← Incoming links (6)

- [index.js](_file/index.js.md)
- [`convert` function](convert-function.md)
- [Local development server](local-development-server.md)
- [OurBigBook CLI](ourbigbook-cli.md)
- [OurBigBook Library environemnt variable](ourbigbook-library-environemnt-variable.md)
- [OurBigBook Web Next.js unit tests](ourbigbook-web-next-js-unit-tests.md)
