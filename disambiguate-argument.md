# `disambiguate` argument

↑ **Parent:** [Common argument](common-argument.md)

Sometimes the short version of a name is ambiguous, and you need to add some extra text to make both its title and ID unique.

For example, the word "Python" could either refer to:
- the programming language: [https://en.wikipedia.org/wiki/Python_(programming_language)](https://en.wikipedia.org/wiki/Python_(programming_language))
- the genus of snakes: [https://en.wikipedia.org/wiki/Python_(genus)](https://en.wikipedia.org/wiki/Python_(genus))

The `disambiguate` [named argument](named-argument.md) helps you deal more neatly with such problems.

Have a look at this example:
```
My favorite snakes are \x[python-genus]{p}!

My favorite programming language is \x[python-programming-language]!

\x[python-genus]{full}

\x[python-programming-language]{full}

= Python
{disambiguate=genus}
{parent=disambiguate-argument}

= Python
{c}
{disambiguate=programming language}
{parent=disambiguate-argument}
{title2=.py}
{wiki}
```
from which we observe how `disambiguate`:
- gets added to the ID after conversion following the same rules as [automatic ID from title](automatic-id-from-title.md)
- shows up on the header between parenthesis, much like Wikipedia, as well as in [`full` internal links](x-full-argument.md)
- does not show up on non-`full` references. This makes it much more likely that you will be able to reuse the title automatically on an [internal link](internal-link.md) without the [`content` argument](content-argument.md): we wouldn't want to say "My favorite programming language is Python (programming language)" all the time, would we?
- gets added to the default [`\H` `wiki` argument](h-wiki-argument.md) inside parenthesis, following Wikipedia convention, therefore increasing the likelihood that you will be able to go with the default Wikipedia value

Besides disambiguating headers, the `disambiguate` argument has a second related application: disambiguating IDs of images. For example:
```
\x[image-the-title-of-my-disambiguate-image]{full=0}

\x[image-the-title-of-my-disambiguate-image-2]{full=0}

\x[image-the-title-of-my-disambiguate-image]{full}

\x[image-the-title-of-my-disambiguate-image-2]{full}

\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{title=The title of my disambiguate image}

\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{title=The title of my disambiguate image}
{disambiguate=2}
```
which renders as:



> [The title of my disambiguate image](#image-the-title-of-my-disambiguate-image)
> 
> [The title of my disambiguate image](#image-the-title-of-my-disambiguate-image-2)
> 
> [Figure 47. "The title of my disambiguate image"](#image-the-title-of-my-disambiguate-image)
> 
> [Figure 48. "The title of my disambiguate image"](#image-the-title-of-my-disambiguate-image-2)
> 
> <a id="image-the-title-of-my-disambiguate-image"></a>
> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)
> 
> **[Figure 47](#image-the-title-of-my-disambiguate-image). The title of my disambiguate image**.
> 
> <a id="image-the-title-of-my-disambiguate-image-2"></a>
> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)
> 
> **[Figure 48](#image-the-title-of-my-disambiguate-image-2). The title of my disambiguate image**.

Note that unlike for headers, `disambiguate` does not appear on the title of images at all. It serves only to create an unique ID that can be later referred to. Headers are actually the only case where `disambiguate` shows up on the visible rendered output. We intend on making this application obsolete however with:

This use case is even more useful when `title-from-src` is enable by default for the [`media-providers`](ourbigbook-json/media-providers.md) entry, so you don't have to repeat titles several times over and over.

## ↑ Ancestors (5)

1. [Common argument](common-argument.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
