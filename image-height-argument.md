# Image `height` argument

↑ **Parent:** [Image argument](image-argument.md)  
🏷️ **Tags:** [Positive nonzero integer argument](positive-nonzero-integer-argument.md)

By default, we fix image heights to `height=315`, and let the `width` be calculated proportionally once the image loads. We therefore ignore the actual image size. This is done to:
- prevent reflows as the page loads images and can determine their actual sizes, especially is the user opens the page at a given ID in the middle of the page
- create a more uniform media experience by default, unless a custom image size is actually needed e.g. if the image needs to be larger
When the [viewport is narrow enough](mobile-guidelines.md), mobile CSS takes over and forces block images to fill 100% of the page width instead, removing the scrollbar.

[Inline images](inline-image.md) on the other hand never get a horizontal scrollbar, they are just always capped at viewport width.

When the `height` argument is given, it changes that default height. Width is still just calculated proportionally to this new custom height.


```
\Image[logo.svg]
{height=150}
```
which renders as:



> <img src="_raw/logo.svg" alt="" height="150">


```
\Image[logo.svg]
{height=550}
```
which renders as:



> <img src="_raw/logo.svg" alt="" height="550">

Here's a very long test image:

<a id="image-very-long-test-image"></a>
<img src="https://upload.wikimedia.org/wikipedia/commons/4/45/Qian_Xuan_-_Early_Autumn.jpg" alt="" height="600">

**[Figure 41](#image-very-long-test-image). Very long test image**. [Source](https://commons.wikimedia.org/wiki/File:Qian_Xuan_-_Early_Autumn.jpg). And some tall inline maths: $a_b$.

Here's a very long inline ![](https://upload.wikimedia.org/wikipedia/commons/4/45/Qian_Xuan_-_Early_Autumn.jpg) test image:

## ↑ Ancestors (5)

1. [Image argument](image-argument.md)
2. [Image](image.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Image `width` argument](image-width-argument.md)
