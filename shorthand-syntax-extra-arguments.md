# Shorthand syntax extra arguments

↑ **Parent:** [Macro with shorthand syntax](macro-with-shorthand-syntax.md)

Shorthand arguments always work by abbreviating:
- the macro name
- one or more of its positional arguments, which are fixed as either [literal or non-literal](literal-arguments.md) for a given shorthand construct
This means that you can add further arguments as usual.

For example, an shorthand code block with an id can be written as:
```
a `b c`{id=ef} g
```
because that is the same as:
```
a \c[b c]{id=ef} g
```
which renders as:



> a <a id="ef"></a>
> `b c` g

So we see that the `b c` argument is the very first argument of `\c`.

Extra arguments must come after the shorthand opening, e.g. the following does not work:
```
a {id=ef}`b c` g
```

This restriction things easy to parse for humans and machines alike.

## ↑ Ancestors (5)

1. [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
2. [Macro shorthand syntax](macro-shorthand-syntax.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
