# JavaScript interface for arguments

↑ **Parent:** [Macro argument](macro-argument.md)

The JavaScript interface sees arguments as follows:
```
function macro_name(args)
```
where args is a dict such that:
- optional arguments have the key/value pairs explicitly given on the call
- mandatory arguments have a key documented by the API, and the value on the call.

  For example, the link API names its arguments `href` and `text`.

## ↑ Ancestors (4)

1. [Macro argument](macro-argument.md)
2. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)
