# `\Q` `description` argument

↑ **Parent:** [`\Q` argument](q-argument.md)  
🏷️ **Tags:** [`description` argument](description-argument.md)

See: [Section "`description` argument"](description-argument.md).

Example with [explicit macro](macro-shorthand-syntax.md):


```
See the: <quote Hamlet what we are>.

\Q[We know what we are, but not what we may be.]
{title=Hamlet what we are}
{description=This quote refers to human's inability to know their own potential, despite understanding their current abilities.}
```
which renders as:



> See the: [Quote 1. "Hamlet what we are"](#quote-hamlet-what-we-are).
> 
> <a id="quote-hamlet-what-we-are"></a>
> > We know what we are, but not what we may be.

Example with [implicit syntax](macro-shorthand-syntax.md):


```
See the: <quote Hamlet what we are implicit>.

> We know what we are, but not what we may be.
{title=Hamlet what we are implicit}
{description=This quote refers to human's inability to know their own potential, despite understanding their current abilities.}
```
which renders as:



> See the: [Quote 2. "Hamlet what we are implicit"](#quote-hamlet-what-we-are-implicit).
> 
> <a id="quote-hamlet-what-we-are-implicit"></a>
> > We know what we are, but not what we may be.

## ↑ Ancestors (5)

1. [`\Q` argument](q-argument.md)
2. [Quotation](quotation.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
