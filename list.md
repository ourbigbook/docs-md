# List

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [Macro with shorthand syntax](macro-with-shorthand-syntax.md)

[Shorthand](macro-shorthand-syntax.md) with `* ` (asterisk space):
```
* a
* b
* c
```
which renders as:



> 
> - a
> - b
> - c

Equivalent saner with [implicit `ul` container](auto-parent.md):
```
\L[a]
\L[b]
\L[c]
```
which renders as:



> 
> - a
> - b
> - c

Equivalent fully sane with explicit container:
```
\Ul[
\L[a]
\L[b]
\L[c]
]
```
which renders as:



> 
> - a
> - b
> - c

The explicit container is required if you want to pass extra arguments properties to the `ul` list macro, e.g. a title and an ID: [Ul 1](#list-my-id):
```
\Ul
{id=list-my-id}
[
\L[a]
\L[b]
\L[c]
]
```
which renders as:



> <a id="list-my-id"></a>
> 
> - a
> - b
> - c

This is the case because without the explicit container in an implicit `ul` list, the arguments would stick to the last list item instead of the list itself.

It is also required if you want ordered lists:
```
\Ol[
\L[first]
\L[second]
\L[third]
]
```
which renders as:



> 
> 1. first
> 1. second
> 1. third

Shorthand nested list with two space indentation:
```
* a
  * a1
  * a2
  * a2
* b
* c
```
which renders as:



> 
> - a
>   - a1
>   - a2
>   - a2
> - b
> - c

The indentation must always be exactly equal to two spaces, anything else leads to errors or unintended output.

Equivalent saner nested lists with implicit containers:
```
\L[
a
\L[a1]
\L[a2]
\L[a2]
]
\L[b]
\L[c]
```
which renders as:



> 
> - a
>   - a1
>   - a2
>   - a2
> - b
> - c

Shorthand list item with a paragraph inside of it:
```
* a
* I have

  Multiple paragraphs.

  * And
  * also
  * a
  * list
* c
```
which renders as:



> 
> - a
> - I have
> 
>   Multiple paragraphs.
> 
> 
>   - And
>   - also
>   - a
>   - list
> - c

Equivalent sane version:
```
\L[a]
\L[
I have

Multiple paragraphs.

\L[And]
\L[also]
\L[a]
\L[list]
]
\L[c]
```
which renders as:



> 
> - a
> - I have
> 
>   Multiple paragraphs.
> 
> 
>   - And
>   - also
>   - a
>   - list
> - c

Shorthand lists may be escaped with a backslash as usual:
```
\* paragraph starting with an asterisk.
```
which renders as:



> \* paragraph starting with an asterisk.

You can also start shorthand lists immediately at the start of a [positional or named argument](positional-vs-named-arguments.md), e.g.:
```
\P[* a
* b
* c
]
```
which renders as:



> 
> - a
> - b
> - c

And now a list outside of [`\OurBigBookExample`](ourbigbookexample.md) to test how it looks directly under [the `\Toplevel` implicit macro](toplevel.md):

- a
- b
- c

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (6)

- [Argument leading and trailing newline removal](argument-leading-and-trailing-newline-removal.md)
- [`Auto_parent` macro property](auto-parent.md)
- [Escape characters](escape-characters.md)
- [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
- [Table](table.md)
