# Positional vs named arguments

↑ **Parent:** [Macro argument](macro-argument.md)

Every argument in OurBigBook is either positional or named.

For example, in a [header](header.md) definition with an ID:
```
= My asdf
{id=asdf qwer}
{scope}
```
which is equivalent to the [explicit](macro-shorthand-syntax.md) version:
```
\H[1][My asdf]
{id=asdf qwer}
{scope}
```
we have:
- two positional argument: `[1]` and `[My asdf]`. Those are surrounded by square brackets `[]` and have no name
- two named arguments: `{id=asdf qwer}` and `{scope}`.

  The first one has name `id`, followed by the separator `=`, followed by the value `asdf qwer`.

  The separator `=` always is optional. If not given, it is equivalent to an empty value, e.g.:
  ```
  {id=}
  ```
  is the same as:
  ```
  {id}
  ```

You can determine if a macro is positional or named by using [`--help-macros`](help-macros.md). Its output contains something like:
```
  "h": {
    "name": "h",
    "positional_args": [
      {
        "name": "level"
      },
      {
        "name": "content"
      }
    ],
    "named_args": {
      "id": {
        "name": "id"
      }
      "scope": {
        "name": "scope"
      }
    },
```
and so we see that `level` and the [`content` argument](content-argument.md) are positional arguments, and `id` and `scope` are named arguments.

Generally, positional arguments are few (otherwise it would be hard to know which is which is which), and are almost always used for a given element so that they save us from typing the name too many times.

The order of positional arguments must of course be fixed, but named arguments can go anywhere. We can even mix positional and named arguments however we want, although this is not advised for clarity.

The following are therefore all equivalent:
```
\H[1][My asdf]{id=asdf qwer}{scope}
\H[1][My asdf]{scope}{id=asdf qwer}
\H{id=asdf qwer}{scope}[1][My asdf]
\H{scope}[1]{id=asdf qwer}[My asdf]
```

Just like named arguments, positional arguments are never mandatory.

**Table of contents**

- [Positional argument](positional-argument.md)
  - [Positional argument default values](positional-argument-default-values.md)
  - [Mandatory positional arguments](mandatory-positional-arguments.md)
- [Named argument](named-argument.md)

## ↑ Ancestors (4)

1. [Macro argument](macro-argument.md)
2. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (5)

- [Escape characters](escape-characters.md)
- [List](list.md)
- [Named argument](named-argument.md)
- [Positional argument](positional-argument.md)
- [Saner](saner.md)
