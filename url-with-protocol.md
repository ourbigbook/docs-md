# URL with protocol

↑ **Parent:** [`\a` `external` argument](a-external-argument.md)

A URL with protocol is a URL that matches the regular expression `^[a-zA-Z]+://`. The following are examples of URLs with protocol:
- `http://cirosantilli.com`
- `https://cirosantilli.com`
- `file:///etc/fstab`
- `ftp://cirosantilli.com`

The following aren't:
- `index.js`
- `../index.js`
- `path/to/index.js`
- `/path/to/index.js`
- `//example.com/path/to/index.js`. This one is a bit tricky. Web browsers would consider this as a [protocol-relative URL](https://stackoverflow.com/questions/28446314/why-use-protocol-relative-urls-at-all), which technically implies a protocol, although that protocol would be different depending how you are viewing the file, e.g. locally through `file://` vs on a with website `https://`.

  For simplicity's sake, we just consider it as a URL without protocol.

## ↑ Ancestors (6)

1. [`\a` `external` argument](a-external-argument.md)
2. [`\a` argument](a-argument.md)
3. [Link](link.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [External link](external-link.md)
