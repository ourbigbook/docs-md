# Image

↑ **Parent:** [Macro](macro.md)

A block image with [capital](block-vs-inline-macros.md) 'i' `Image` showcasing most of the image properties [Figure 26. "The title of my image"](#image-my-test-image).
```
Have a look at this amazing image: \x[image-my-test-image].

\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{title=The title of my image}
{id=image-my-test-image}
{width=600}
{height=200}
{source=https://en.wikipedia.org/wiki/File:Tianasquare.jpg}
{description=The description of my image.}
```
which renders as:



> Have a look at this amazing image: [Figure 26. "The title of my image"](#image-my-test-image).
> 
> <a id="image-my-test-image"></a>
> <img src="_raw/Tank_man_standing_in_front_of_some_tanks.jpg" alt="" width="600" height="200">
> 
> **[Figure 26](#image-my-test-image). The title of my image**. [Source](https://en.wikipedia.org/wiki/File:Tianasquare.jpg). The description of my image.

This exemplifies the following parameters:
- `title`: analogous to the [`\H` `title` argument](h-title-argument.md). Shows up preeminently, and sets a default ID if one is not given. It is recommended that you don't add a period `.` to it, as that would show in [internal links](internal-link.md)
- [image `description` argument](image-description-argument.md)
- [`source`](image-source-argument.md): a standardized way to credit an image by linking to a URL that contains further image metadata
For further discussion on the effects of ID see: [Section "Image ID"](image-id.md).

And this is how you make an [inline image](inline-image.md) inline one with lower case `i`:
```
My inline \image[Tank_man_standing_in_front_of_some_tanks.jpg][test image] is awesome.
```
which renders as:



> My inline ![test image](_raw/Tank_man_standing_in_front_of_some_tanks.jpg) is awesome.

[Inline images](inline-image.md) can't have captions.

And now for an image outside of [`\OurBigBookExample`](ourbigbookexample.md) to test how it looks directly under [the `\Toplevel` implicit macro](toplevel.md): [Figure 27](#image-my-test-image-toplevel).

<a id="image-my-test-image-toplevel"></a>
![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)

**[Figure 27](#image-my-test-image-toplevel)**

**Table of contents**

- [Image ID](image-id.md)
  - [Image caption](image-caption.md)
- [Where to store images](where-to-store-images.md)
  - [Store images inside the repository itself](store-images-inside-the-repository-itself.md)
  - [Store images in a separate media repository](store-images-in-a-separate-media-repository.md)
    - [Store images in a separate media repository and track it as a git submodule](store-images-in-a-separate-media-repository-and-track-it-as-a-git-submodule.md)
  - [Store images in Wikimedia Commons](store-images-in-wikimedia-commons.md)
- [Image lazy loading](image-lazy-loading.md)
- [Background color of transparent images](background-color-of-transparent-images.md)
- [Image generators](image-generators.md)
- [Block and inline images](block-and-inline-images.md)
  - [Inline image](inline-image.md)
- [Image argument](image-argument.md)
  - [Image `border` argument](image-border-argument.md)
  - [Image `description` argument](image-description-argument.md)
  - [Image `external` argument](image-external-argument.md)
  - [Image `height` argument](image-height-argument.md)
  - [Image `link` argument](image-link-argument.md)
  - [Image `source` argument](image-source-argument.md)
  - [Image `src` argument](image-src-argument.md)
  - [Image `title` argument](image-title-argument.md)
  - [Image `width` argument](image-width-argument.md)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (19)

- [Boolean argument](boolean-argument.md)
- [`description` argument](description-argument.md)
- [`--embed-resources`](embed-resources.md)
- [Features](features.md)
- [`\H` `file` argument](h-file-argument.md)
- [`\H` `splitDefault` argument](h-splitdefault-argument.md)
- [`\H` `title2` argument](h-title2-argument.md)
- [`Id` output format](id-output-format.md)
- [Internal link title link removal](internal-link-title-link-removal.md)
- [Mathematics](mathematics.md)
- [`Media-providers`](ourbigbook-json/media-providers.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
- [Produce a standalone HTML file](produce-a-standalone-html-file.md)
- [Table](table.md)
- [Template variable](template-variable.md)
- [`title` argument](title-argument.md)
- [Video](video.md)
- [`\x` `full` argument](x-full-argument.md)
- [`\x` within `title` restrictions](x-within-title-restrictions.md)
