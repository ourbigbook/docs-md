# Comment

↑ **Parent:** [Macro](macro.md)

The `Comment` and `comment` macros are regular macros that does not produce any output. Capitalization is explained at: [Section "Block vs inline macros"](block-vs-inline-macros.md).

You will therefore mostly want to use it with a [literal argument](literal-arguments.md), which will, as for any other macro, ignore any macros inside of it.
```
Before comment.

\Comment[[
Inside comment.
]]

After comment.
```
which renders as:



> Before comment.
> 
> After comment.

And an inline one:
```
My inline \comment[[inside comment]] is awesome.

\comment[[inside comment]] inline at the start.
```
which renders as:



> My inline  is awesome.
> 
>  inline at the start.

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Block vs inline macros](block-vs-inline-macros.md)
