# Code block

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [Macro with shorthand syntax](macro-with-shorthand-syntax.md)

Inline code (code that should appear in the middle of a paragraph rather than on its own line) is done with a single backtick (`` ` ``) [macro shorthand syntax](macro-shorthand-syntax.md):
```
My inline `x = 'hello\n'` is awesome.
```
which renders as:



> My inline `x = 'hello\n'` is awesome.

and block code (code that should appear on their own line) is done with two or more backticks (``` `` ```):
```
``
f() {
  return 'hello\n';
}
``
```
which renders as:



> ```
> f() {
>   return 'hello\n';
> }
> ```

The sane version of inline code is a lower case `c`:
```
My inline \c[[x = 'hello\n']] is awesome.
```
which renders as:



> My inline `x = 'hello\n'` is awesome.

and the sane version of block math is with an upper case `C`:
```
\C[[
f() {
  return 'hello\n';
}
]]
```
which renders as:



> ```
> f() {
>   return 'hello\n';
> }
> ```

The capital vs lower case theme is also used in other elements, see: [block vs inline macros](block-vs-inline-macros.md).

If the content of the sane code block has many characters that you would need to [escape](escape-characters.md), you will often want to use [literal arguments](literal-arguments.md), which work just like the do for any other argument. For example:
```
\C[[[
A paragraph.

\C[[
And now, some long, long code, with lots
of chars that you would need to escape:
\ [  ] {  }
]]

A paragraph.
]]]
```
which renders as:



> ```
> A paragraph.
> 
> \C[[
> And now, some long, long code, with lots
> of chars that you would need to escape:
> \ [  ] {  }
> ]]
> 
> A paragraph.
> ```

Note that the initial newline is skipped automatically in code blocks, just as for any other element, due to: [argument leading newline removal](argument-leading-and-trailing-newline-removal.md), so you don't have to worry about it.

The distinction between inline `\c` and block `\C` code blocks is needed because in HTML, [`pre` cannot go inside `P`](https://stackoverflow.com/questions/5371787/can-i-have-a-pre-tag-inside-a-p-tag-in-tumblr/58603596#58603596).

We could have chosen to do some magic to differentiate between them, e.g. checking if the block is the only element in a paragraph, but we decided not to do that to keep the language saner.

And now a code block outside of [`\OurBigBookExample`](ourbigbookexample.md) to test how it looks directly under [the `\Toplevel` implicit macro](toplevel.md):

```
Hello

Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello
    HelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHello
Hello
```

Now with short description with math and underline:

```
Hello

Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello
    HelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHelloHello
Hello
```

And now a very long inline code: `Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello Hello`

**Table of contents**

- [`\C` argument](c-argument.md)
  - [`\C` `description` argument](c-description-argument.md)
  - [`\C` `title` argument](c-title-argument.md)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (8)

- [Block vs inline macros](block-vs-inline-macros.md)
- [`description` argument](description-argument.md)
- [Escape characters](escape-characters.md)
- [Line break](line-break.md)
- [Literal arguments](literal-arguments.md)
- [Macro shorthand syntax](macro-shorthand-syntax.md)
- [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
