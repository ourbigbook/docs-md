# Order of reported errors

↑ **Parent:** [Error reporting](error-reporting.md)

One important philosophy of the error reporting is that the very first message should be the root cause of the problem whenever possible: users should not be forced to search a hundred messages to find the root cause. In this way, the procedure:
- solve the first error
- reconvert
- solving the new first error
- reconvert
- etc.
should always deterministically lead to a resolution of all problems.

Error messages are normally sorted by file, line and column, regardless of which conversion stage they happened (e.g. a tokeniser error first gets reported before a parser error).

There is however one important exception to that: broken [internal links](internal-link.md) are always reported last.

For example, consider the following syntactically wrong document:
```
= a

\x[b]

``
== b
```
Here we have an unterminated code block at line 5.

However, this unterminated code block leads the header `b` not to be seen, and therefore the reference `\x[b]` on line 3 to fail.

Therefore, if we sorted naively by line, the broken reference would shoe up first:
```
error: tmp.bigb:3:3: internal link to unknown id: "b"
error: tmp.bigb:5:1: unterminated literal argument
```

But in a big document, this case could lead to hundreds of undefined references to show up before the actual root unterminated literal problem.:
```
error: tmp.bigb:3:3: internal link \x to unknown id: "b"
error: tmp.bigb:4:3: internal link \x to unknown id: "b"
error: tmp.bigb:5:3: internal link \x to unknown id: "b"
...
error: tmp.bigb:1000:1: unterminated literal argument
```

Therefore, we force undefined references to show up last to prevent this common problem:
```
error: tmp.bigb:1000:1: unterminated literal argument
error: tmp.bigb:3:3: intenal link \x to unknown id: "b"
error: tmp.bigb:4:3: intenal link \x to unknown id: "b"
error: tmp.bigb:5:3: intenal link \x to unknown id: "b"
...
```

## ↑ Ancestors (3)

1. [Error reporting](error-reporting.md)
2. [Tooling](tooling.md)
3. [OurBigBook Project](split.md)
