# Positional argument default values

↑ **Parent:** [Positional argument](positional-argument.md)

Most positional arguments will default to an empty string if not given.

However, some positional arguments can have special effects if not given.

For example, an anchor with the first positional argument present (the URL), but not the second positional argument (the link text) as in:
```
\a[http://example.com]
```
which renders as:



> [http://example.com](http://example.com)

has the special effect of generating automatic links as in:
```
\a[http://example.com][http://example.com]
```

This can be contrasted with named arguments, for which there is always a default value, notably for [boolean arguments](boolean-argument.md).

See also: [Section "Link"](link.md).

## ↑ Ancestors (6)

1. [Positional argument](positional-argument.md)
2. [Positional vs named arguments](positional-vs-named-arguments.md)
3. [Macro argument](macro-argument.md)
4. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)
