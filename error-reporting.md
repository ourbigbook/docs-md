# Error reporting

↑ **Parent:** [Tooling](tooling.md)

A lot of effort has been put into making error reporting as good as possible in OurBigBook, to allow authors to quickly find what is wrong with their source code.

Error reporting is for example tested with `assert_error` tests in [test.js](test.js).

Please report any error reporting bug you find, as it will be seriously tracked under the: [`error-reporting` label](https://github.com/ourbigbook/ourbigbook/issues?q=label%3Aerror-reporting+).

Notably, OurBigBook should never throw an exception due to a syntax error, as that prevents error messages from being output at all.

**Table of contents**

- [Order of reported errors](order-of-reported-errors.md)

## ↑ Ancestors (2)

1. [Tooling](tooling.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Features](features.md)
