# Image `description` argument

↑ **Parent:** [Image argument](image-argument.md)  
🏷️ **Tags:** [`description` argument](description-argument.md), [Named argument](named-argument.md)

The `description` argument similar to the [image `title` argument](image-title-argument.md) argument, but allows allowing longer explanations without them appearing in [internal links](internal-link.md) to the image.

For example, consider:
```
See this image: \x[image-description-argument-test-1].

\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{title=Tank man standing in front of some tanks}
{id=image-description-argument-test-1}
{description=Note how the tanks are green.}
{source=https://en.wikipedia.org/wiki/File:Tianasquare.jpg}
```
which renders as:



> See this image: [Figure 39. "Tank man standing in front of some tanks"](#image-description-argument-test-1).
> 
> <a id="image-description-argument-test-1"></a>
> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)
> 
> **[Figure 39](#image-description-argument-test-1). Tank man standing in front of some tanks**. [Source](https://en.wikipedia.org/wiki/File:Tianasquare.jpg). Note how the tanks are green.

In this example, the reference `\x[image-description-argument-test-1]` expands just to

> Tank man standing in front of some tanks

and does not include the description, which only shows on the image.

The description can be as large as you like. If it gets really large however, you might want to consider moving the image to its own header to keep things slightly saner. This will be especially true after we eventually do: [https://github.com/ourbigbook/ourbigbook/issues/180](https://github.com/ourbigbook/ourbigbook/issues/180).

If the description contains any element that would take its own separate line, like multiple paragraphs or a list, we automatically add a line grouping the description with the corresponding image to make that clearer, otherwise it can be hard to know which title corresponds to a far away image. Example with multiple paragraphs:
```
Stuff before the image.

\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{title=Tank man standing in front of some tanks}
{id=image-description-argument-test-2}
{source=https://en.wikipedia.org/wiki/File:Tianasquare.jpg}
{description=Note how the tanks are green.

But the shirt is white.}

Stuff after the image description.
```
which renders as:



> Stuff before the image.
> 
> <a id="image-description-argument-test-2"></a>
> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)
> 
> **[Figure 40](#image-description-argument-test-2). Tank man standing in front of some tanks**. [Source](https://en.wikipedia.org/wiki/File:Tianasquare.jpg). Note how the tanks are green.
> 
> But the shirt is white.
> 
> ---
> 
> Stuff after the image description.

We recommend adding a period or other punctuation to the end of every description.

## ↑ Ancestors (5)

1. [Image argument](image-argument.md)
2. [Image](image.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Image](image.md)
- [Image caption](image-caption.md)
- [Image ID](image-id.md)
