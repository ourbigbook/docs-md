# Escape characters

↑ **Parent:** [Macro argument](macro-argument.md)

Every character that cannot be a [macro identifier](macro-identifier.md) can be escaped with a backslash `\`. If you try to escape a macro identifier it of course treats the thing as a macro instead and fails, e.g. in `\a` it would try to use a macro called `\a`, not escape the character `a`.

For some characters, escaping or not does not make any difference because they don't have any meaning to [OurBigBook Markup](ourbigbook-markup.md), e.g. currently `%` is always the exact same as `\%`.

But in [non-literal macro arguments](literal-arguments.md), you have to use a backslash to escape the following if you want them to not have any magical meaning:
- `\`: backslashes start macros
- `\[` and `\]`: open and close [positional macro arguments](positional-vs-named-arguments.md)
- `\{` and `\}`: open and close [optional macro arguments](positional-vs-named-arguments.md)
- escapes for [macros with shorthand syntax](macro-with-shorthand-syntax.md):
  - `<` (open angle brackets, less than sign): [macro shorthand syntax](macro-shorthand-syntax.md) for [shorthand internal links](shorthand-internal-link.md)
  - `$` (dollar sign): [macro shorthand syntax](macro-shorthand-syntax.md) for [mathematics](mathematics.md)
  - `` ` `` (backtick): [macro shorthand syntax](macro-shorthand-syntax.md) for [code blocks](code-block.md)
  - `#` (hash): [shorthand topic links](shorthand-topic-link.md)

Furthermore, only at:
- at the start of the document
- after a newline
- at the start of a new argument
you must also escape the following [macros with shorthand syntax](macro-with-shorthand-syntax.md):
- `* ` for shorthand [lists](list.md)
- `| ` and `|| ` for shorthand [tables](table.md)
- `= ` for shorthand [headers](header.md)

The escape rules for literal arguments are described at: [Section "Literal arguments"](literal-arguments.md).

This is good for short arguments of regular text, but for longer blocks like [code blocks](code-block.md) or [mathematics](mathematics.md), you may want to use [literal arguments](literal-arguments.md)

## ↑ Ancestors (4)

1. [Macro argument](macro-argument.md)
2. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [Code block](code-block.md)
- [`--escape-literal`](escape-literal.md)
- [Line break](line-break.md)
- [Mathematics](mathematics.md)
