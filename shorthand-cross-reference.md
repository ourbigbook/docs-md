# Shorthand cross reference

↑ **Parent:** [Internal link](internal-link.md)  
🏷️ **Tags:** [Shorthand macro syntax](macro-shorthand-syntax.md)

When you use an [shorthand internal link](shorthand-internal-link.md) (`<>`) such as in:
```
<Internal links> are awesome.
```
which renders as:



> [Internal links](internal-link.md) are awesome.

it gets expanded exactly to the sane equivalent:
```
\x[Internal links]{magic} are alwasome
```
so we see that the [`\x` `magic` argument](x-magic-argument.md) gets added. It is that argument that for example adds the missing `-`, and removes the pluralization to find the correct ID `internal-link`.  For more details, see the documentation of the [`\x` `magic` argument](x-magic-argument.md).

Like other [shorthand](macro-shorthand-syntax.md) constructs, [shorthand internal links](shorthand-internal-link.md) are exactly equivalent to the sane version, so you can just add other arguments after the construct, e.g.:
```
<Internal links>{full} are awesome.
```
which renders as:



> [Section "Internal link"](internal-link.md) are awesome.

which gets converted to exact the same as the sane:
```
\x[internal-link]{full} are awesome.
```
which renders as:



> [Section "Internal link"](internal-link.md) are awesome.

## ↑ Ancestors (4)

1. [Internal link](internal-link.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)
