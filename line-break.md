# Line break

↑ **Parent:** [Macro](macro.md)

The `\br` macro inserts a visible newline between two lines without creating a paragraph, for example:
```
ab\br[]cd
```
which renders as:



> ab  
> cd

Note that here `[]` is an [`empty` macro argument](empty-macro-argument.md) used for convenience to separate the `\br` from the `cd` text that immediately follows.

The recommended syntax is the shorthand version which simply uses a newline as in:
```
ab
cd
```
which renders as:



> ab  
> cd

Note that the newline only works as a line break if surrounded by two [inline macros](inline-macro.md) as mentioned at [newline removal](newline-removal.md).

If for some reason you want to have an actual literal newline in your output outside of [literal arguments](literal-arguments.md), just [escape the newline with a backslash as for escaping anything else](escape-characters.md).

There is basically just one application for line breaks: poetry, which would be too ugly with [code blocks](code-block.md) due to fixed width font:
```
Even as the sun with purple-coloured face
Had taken his last leave of the weeping morn,
Rose-cheeked Adonis tried him to the chase;
Hunting he loved, but love he laughed to scorn;
Sick-thoughted Venus makes amain unto him,
And like a bold-faced suitor begins to woo him.

"Thrice fairer than myself," thus she began,
The field's chief flower, sweet above compare,
Stain to all nymphs, more lovely than a man,
More white and red than doves or roses are;
Nature that made thee, with herself at strife,
Saith that the world hath ending with thy life.
```
which renders as:



> Even as the sun with purple-coloured face  
> Had taken his last leave of the weeping morn,  
> Rose-cheeked Adonis tried him to the chase;  
> Hunting he loved, but love he laughed to scorn;  
> Sick-thoughted Venus makes amain unto him,  
> And like a bold-faced suitor begins to woo him.
> 
> "Thrice fairer than myself," thus she began,  
> The field's chief flower, sweet above compare,  
> Stain to all nymphs, more lovely than a man,  
> More white and red than doves or roses are;  
> Nature that made thee, with herself at strife,  
> Saith that the world hath ending with thy life.

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Adding your first macro](adding-your-first-macro.md)
- [Newline removal](newline-removal.md)
