# OurBigBook Markup quick start

↑ **Parent:** [OurBigBook Markup](ourbigbook-markup.md)

[Paragraphs](paragraph.md) are made by simplifying adding an empty line, e.g.:
```
My first paragraph.

And now my second paragraph.

Third one to finish.
```
which renders as:



> My first paragraph.
> 
> And now my second paragraph.
> 
> Third one to finish.

[Headers](header.md) are created by starting the line with equal signs. The more equal signs the deeper you are, e.g.:
```
= Animal

== Mammal

=== Dog

=== Cat

== Bird

=== Pigeon

=== Chicken
```
On [OurBigBook Web](ourbigbook-web.md), the toplevel header of each page goes into a separate title box, so there things would just look like:
- title box: "Animal"
- body:
  ```
  == Mammal

  === Dog

  === Cat

  == Bird

  === Pigeon

  === Chicken
  ```

You can can use any header as a [tag](h-tag-argument.md) of any other header, e.g.:
```
= Animal

== Dog
{tag=Cute animal}

== Turtle
{tag=Ugly animal}

== Animal cuteness

=== Cute animal

=== Ugly animal
```

Headers have several powerful features that you can read more about under [`\H` arguments](h-arguments.md), e.g. [`\H` `synonym` argument](h-synonym-argument.md) and [`\H` `disambiguate` argument](disambiguate-argument.md).

To [link to any of your other pages](internal-link.md), you can use angle brackets (less than/greater than) signs:
```
I have a <cute animal>. <Birds> are too noisy.
```
Note how [capitalization and pluralization generally just work](internal-link-title-inflection.md).

To use a custom link text on a reference, use the following syntax:
```
I have a <cute animal>[furry animal]. <Birds>[feathery animals] are too noisy.
```

External links can be input directly as:
```
This is a great website: https://example.com

I really like https://example.com[this website].
```
which renders as:



> This is a great website: [https://example.com](https://example.com)
> 
> I really like [this website](https://example.com).

[Code blocks](code-block.md) are done with backticks `` ` ``. With just one backtick, you get a code block inside the text:
```
The function call `f(x + 1, "abc")` is wrong.
```
which renders as:



> The function call `f(x + 1, "abc")` is wrong.

and with two ore more backticks you get a code block on its own line, and possibly with multiple code lines:
```
The function:
``
function f(x, s) {
  return x + s
}
``
is wrong.
```
which renders as:



> The function:
> ```
> function f(x, s) {
>   return x + s
> }
> ```
> is wrong.

[Mathematics](mathematics.md) syntax is very similar to code blocks, you can just enter you LaTeX code in it:
```
The number $\sqrt{2}$ is irrational.

The same goes for:
$$
\frac{1}{\sqrt{2}}
$$
```
which renders as:



> The number $\sqrt{2}$ is irrational.
> 
> The same goes for:
> 
> $$
> \frac{1}{\sqrt{2}}
> $$

We also have [a bunch of predefined macros from popular packages](built-in-latex-macros.md), e.g. `\dv` from the [`physics` package](https://mirrors.ibiblio.org/CTAN/macros/latex/contrib/physics/physics.pdf) for derivatives:
```
$$
\dv{x^2}{x} = 2x
$$
```
which renders as:



> $$
> \dv{x^2}{x} = 2x
> $$

You can [refer](internal-link.md) to specific equations like this:
```
As shown in <equation Very important equation>, this is true.

$$
\frac{1}{\sqrt{2}}
$$
{title=Very important equation}
```
which renders as:



> As shown in [Equation 3. "Very important equation"](#equation-very-important-equation), this is true.
> 
> <a id="equation-very-important-equation"></a>
> $$
> \frac{1}{\sqrt{2}}
> $$

[Images](image.md) and [videos](video.md) are also easy to add and [refer](internal-link.md) to:
```
As shown at <image Cute chicken chick>, chicks are cute.

\Image[https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/H%C3%BChnerk%C3%BCken_02.jpg/800px-H%C3%BChnerk%C3%BCken_02.jpg?20200716091201]
{title=Cute chicken chick}

\Video[https://www.youtube.com/watch?v=j_fl4xoGTKU]
{title=Top Down 2D Continuous Game by Ciro Santilli (2018)}
```
which renders as:



> As shown at [Figure 21. "Cute chicken chick"](#image-cute-chicken-chick), chicks are cute.
> 
> <a id="image-cute-chicken-chick"></a>
> ![](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/H%C3%BChnerk%C3%BCken_02.jpg/800px-H%C3%BChnerk%C3%BCken_02.jpg?20200716091201)
> 
> **[Figure 21](#image-cute-chicken-chick). Cute chicken chick**. [Source](https://commons.wikimedia.org/wiki/File:H%C3%BChnerk%C3%BCken_02.jpg?20200716091201).
> 
> <a id="video-top-down-2d-continuous-game-by-ciro-santilli-2018"></a>
> **[Video 5](#video-top-down-2d-continuous-game-by-ciro-santilli-2018). Top Down 2D Continuous Game by Ciro Santilli (2018)** [Source](https://www.youtube.com/watch?v=j_fl4xoGTKU).

Images can take a bunch of options, about which you can read more about at [image arguments](image-argument.md). Most should be self explanatory, here is an image with a bunch of useful arguments:
```
\Image[https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/H%C3%BChnerk%C3%BCken_02.jpg/800px-H%C3%BChnerk%C3%BCken_02.jpg?20200716091201]
{title=Ultra cute chicken chick}
{description=
The chicken is yellow, and the hand is brown.

The background is green.
}
{border}
{height=400}
{source=https://commons.wikimedia.org/wiki/File:H%C3%BChnerk%C3%BCken_02.jpg}
```
which renders as:



> <a id="image-ultra-cute-chicken-chick"></a>
> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/H%C3%BChnerk%C3%BCken_02.jpg/800px-H%C3%BChnerk%C3%BCken_02.jpg?20200716091201" alt="" height="400">
> 
> **[Figure 22](#image-ultra-cute-chicken-chick). Ultra cute chicken chick**. [Source](https://commons.wikimedia.org/wiki/File:H%C3%BChnerk%C3%BCken\_02.jpg). The chicken is yellow, and the hand is brown.
> 
> The background is green.
> 
> ---

[Lists](list.md) are written by starting the line with an asterisk `*`:
```
* first item
* second item
* and the third
```
which renders as:



> 
> - first item
> - second item
> - and the third

A nested list:
```
* first item
  * first item version 1
  * first item version 2
    * first item version 2 1
    * first item version 2 2
* second item
* and the third
```
which renders as:



> 
> - first item
>   - first item version 1
>   - first item version 2
>     - first item version 2 1
>     - first item version 2 2
> - second item
> - and the third

Lists items can contain any markup, e.g. paragraphs. You just need to keep the same number of spaces, e.g.:
```
* first item.

  Second paragraph of first item.

  And a third one.
* second item
  * second item v1

    Another paragraph in second item v1
  * second item v2
```
which renders as:



> 
> - first item.
> 
>   Second paragraph of first item.
> 
>   And a third one.
> - second item
>   - second item v1
> 
>     Another paragraph in second item v1
>   - second item v2

[Tables](table.md) are not very different from lists. We use double pipes for headers `||`, and a single pipe `|` for regular rows:
```
|| City
|| Sales

| Salt Lake City
| 124,00

| New York
| 1,000,000
```
which renders as:



> | City | Sales |
> | --- | --- |
> | Salt Lake City | 124,00 |
> | New York | 1,000,000 |

To add a title we need to use an explicit `\Table` macro as in:
```
See <table Sales per city> for more information.

\Table
{title=Sales per city}
[
|| City
|| Sales

| Salt Lake City
| 124,00

| New York
| 1,000,000
]
```
which renders as:



> See [Table 1. "Sales per city"](#table-sales-per-city) for more information.
> 
> <a id="table-sales-per-city"></a>
> | City | Sales |
> | --- | --- |
> | Salt Lake City | 124,00 |
> | New York | 1,000,000 |

## ↑ Ancestors (2)

1. [OurBigBook Markup](ourbigbook-markup.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Quick start](quick-start.md)
