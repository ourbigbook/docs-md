# Image `width` argument

↑ **Parent:** [Image argument](image-argument.md)  
🏷️ **Tags:** [Positive nonzero integer argument](positive-nonzero-integer-argument.md)

This argument is meant to be analogous to the [Image `height` argument](image-height-argument.md) but for images.

Usage of this argument is generally discouraged, as we always set the default image height by default, so that also passing a width is either unnecessary or may lead to changes in the image's correct aspect ratio.


```
\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{width=150}
```
which renders as:



> <img src="_raw/Tank_man_standing_in_front_of_some_tanks.jpg" alt="" width="150">


```
\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{width=550}
```
which renders as:



> <img src="_raw/Tank_man_standing_in_front_of_some_tanks.jpg" alt="" width="550">

## ↑ Ancestors (5)

1. [Image argument](image-argument.md)
2. [Image](image.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
