# Image `link` argument

↑ **Parent:** [Image argument](image-argument.md)  
🏷️ **Tags:** [Named argument](named-argument.md)

If given, make clicking an image go to the specified URL rather than the image's URL as is the default.

By default, clicking on a rendered image links to the URL of the image itself. E.g. clicking:
```
\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
```
which renders as:



> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)

would open [Tank_man_standing_in_front_of_some_tanks.jpg](Tank_man_standing_in_front_of_some_tanks.jpg) as produces `img` surrounded by something like `a href="Tank_man_standing_in_front_of_some_tanks.jpg"`.

If insetad we want the image to point to a custom URL, e.g. [https://ourbigbook.com](https://ourbigbook.com) we could instead write:
```
\Image[Tank_man_standing_in_front_of_some_tanks.jpg]{link=https://ourbigbook.com}
```
which renders as:



> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)

and now clicking the image leads to [https://ourbigbook.com](https://ourbigbook.com) instead.

## ↑ Ancestors (5)

1. [Image argument](image-argument.md)
2. [Image](image.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
