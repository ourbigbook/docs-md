# Image ID

↑ **Parent:** [Image](image.md)

Here is an image without a [description](image-description-argument.md) but with an ID so we can link to it: [Figure 28](#image-my-test-image-2).
```
Have a look at this amazing image: \x[image-my-test-image-2].

\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{id=image-my-test-image-2}
```
which renders as:



> Have a look at this amazing image: [Figure 28](#image-my-test-image-2).
> 
> <a id="image-my-test-image-2"></a>
> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)
> 
> **[Figure 28](#image-my-test-image-2)**

This works because [`full` is the default internal link style for `Image`](x-full-argument.md), otherwise the link text would be empty since there is no `title`, and OurBigBook would raise an error.

OurBigBook can optionally deduce the title from the basename of the `src` argument if the `titleFromSrc` [boolean argument](boolean-argument.md) is given, or if `title-from-src` is set as the default [media provider](ourbigbook-json/media-providers.md) for the media type:
```
Have a look at this amazing image: \x[image-tank-man-standing-in-front-of-some-tanks].

\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{titleFromSrc}
```
which renders as:



> Have a look at this amazing image: [Figure 29. "Tank man standing in front of some tanks."](#image-tank-man-standing-in-front-of-some-tanks).
> 
> <a id="image-tank-man-standing-in-front-of-some-tanks"></a>
> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)
> 
> **[Figure 29](#image-tank-man-standing-in-front-of-some-tanks). Tank man standing in front of some tanks.**

**Table of contents**

- [Image caption](image-caption.md)

## ↑ Ancestors (4)

1. [Image](image.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Image](image.md)
- [Image caption](image-caption.md)
- [`Media-providers`](ourbigbook-json/media-providers.md)
