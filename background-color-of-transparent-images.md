# Background color of transparent images

↑ **Parent:** [Image](image.md)

For the love of God, there is no standardized for SVG to set its background color without a rectangle? [https://stackoverflow.com/questions/11293026/default-background-color-of-svg-root-element](https://stackoverflow.com/questions/11293026/default-background-color-of-svg-root-element) `viewport-fill` was just left in limbo?

And as a result, many many many SVG online images that you might want to reuse just rely on white pages and don't add that background rectangle.

Therefore for now we just force white background on [our default CSS](overview-of-files-in-this-repository.md) of block images, which is what most SVGs will work with. Otherwise, you can lose the entire image to our default black background.

For [inline images](inline-image.md) however, a white background would also be very distracting compared to the nearby inline text, and it would prevent the use case of making rounded smileys, so for now we are just not forcing the background color in that case.

At some point we might just add a `color` argument to set the background color to an arbitrary value so that authors can decide what is better for each image.

## ↑ Ancestors (4)

1. [Image](image.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)
