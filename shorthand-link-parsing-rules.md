# Shorthand link parsing rules

↑ **Parent:** [Link](link.md)

Shorthand start at any of the recognized protocols are the ones shown at: [Section "Known URL protocols"](known-url-protocols.md).
- `http://`
- `https://`
absolutely anywhere if not escaped, e.g.:
```
ahttp://example.com
```
renders something like:
```
a <a href="http://example.com">
```
To prevent expansion, you have to escape the protocol with a backslash `\\`, e.g.:
```
\http://example.com
```
Empty domains like:
```
http://
```
don't becomes links however. But this one does:
```
http://a
```

Shorthand links end when any [shorthand link termination character](shorthand-link-termination-character.md) is found.

As a consequence, to have an shorthand link followed immediately by a punctuation like a period you should use an empty argument as in:
```
Check out this website: http://example.com[].
```
which renders as:



> Check out this website: [http://example.com](http://example.com).

otherwise the punctuation will go in it. Another common use case is:
```
As mentioned on the tutorial (http://example.com[see this link]).
```
which renders as:



> As mentioned on the tutorial ([see this link](http://example.com)).

If you want your link to include one of the terminating characters, e.g. `]`, all characters can be escaped with a backslash, e.g.:
```
Hello http://example.com/\]a\}b\\c\ d world.
```
which renders as:



> Hello [http://example.com/]a}b\c d](http://example.com/]a}b\c d) world.

Note that the `http://example.com` inside `\a[http://example.com]` only works because we do some post-processing magic that prevents its expansion, otherwise the link would expand twice:
```
\P[http://example.com]

\a[http://example.com]
```
which renders as:



> [http://example.com](http://example.com)
> 
> [http://example.com](http://example.com)

This magic can be observed with [`--help-macros`](help-macros.md) by seeing that the `href` argument of the `a` macro has the property:
```
"elide_link_only": true,
```

**Table of contents**

- [Shorthand link termination character](shorthand-link-termination-character.md)

## ↑ Ancestors (4)

1. [Link](link.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [Known URL protocols](known-url-protocols.md)
- [Link](link.md)
- [Shorthand link termination character](shorthand-link-termination-character.md)
- [Shorthand topic links with a single word](shorthand-topic-links-with-a-single-word.md)
