# Escapes in macro shorthands

↑ **Parent:** [Macro with shorthand syntax](macro-with-shorthand-syntax.md)

Literal backticks and dollar signs can be produced witha backslash escape as in:
```
a \` \$ b
```
which renders as:



> a \` $ b

It is not possible to escape backticks (`` ` ``) inside an shorthand inline code, or dollar signs (`$`) in shorthand math.

The design reason for that is because multiple backticks produce block code.

The upside is that then you don't have to escape anything else, e.g. backslashes (`\`) are rendered literally.

The only way to do it is to use the sane syntax instead:
```
a \c[[b ` c]] d

a \m[[\sqrt{\$4}]] d
```
which renders as:



> a ``b ` c`` d
> 
> a $\sqrt{\$4}$ d

Within block code and math, you can just add more separators:
````
```
code with two backticks
``
nice
```
````
which renders as:



> ```
> code with two backticks
> ``
> nice
> ```

## ↑ Ancestors (5)

1. [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
2. [Macro shorthand syntax](macro-shorthand-syntax.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
