# unsafeXss

↑ **Parent:** [Security](security.md)

OurBigBook HTML output is designed to be XSS safe by default, any non-XSS safe constructs must be enabled with a non-default flag or setting, see: [unsafeXss](unsafexss.md).

Of course, we are walking on eggs, and this is hard to assert, so the best thing to do later on will be to parse the output e.g. with [`DOMParser`](https://developer.mozilla.org/en-US/docs/Web/API/DOMParser) to ensure that it is valid and does not contain any `script` tags, but it is not as simple as that: [https://stackoverflow.com/questions/37435077/execute-javascript-for-xss-without-script-tags/61588322#61588322](https://stackoverflow.com/questions/37435077/execute-javascript-for-xss-without-script-tags/61588322#61588322)

XSS unsafe constructs lead to errors by default. XSS unsafe constructs can be allowed [from the command line](ourbigbook-cli.md) with:
```
./ourbigbook --unsafe-xss
```
or from the [`ourbigbook.json`](ourbigbook-json.md) file with an entry of form:
```
"unsafeXss": true
```

**Table of contents**

- [XSS unsafe macro](xss-unsafe-macro.md)

## ↑ Ancestors (2)

1. [Security](security.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Passthrough](passthrough.md)
- [UnsafeXss](unsafexss.md)
- [XSS unsafe macro](xss-unsafe-macro.md)
