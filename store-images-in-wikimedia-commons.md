# Store images in Wikimedia Commons

↑ **Parent:** [Where to store images](where-to-store-images.md)

Wikimedia Commons is another great possibility to upload your images to:
```
\Image[https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Gel_electrophoresis_insert_comb.jpg/450px-Gel_electrophoresis_insert_comb.jpg]
{source=https://commons.wikimedia.org/wiki/File:Gel_electrophoresis_insert_comb.jpg}
```
which renders as:



> ![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Gel_electrophoresis_insert_comb.jpg/450px-Gel_electrophoresis_insert_comb.jpg)
> 
> **[Figure 34](#_1403)** [Source](https://commons.wikimedia.org/wiki/File:Gel\_electrophoresis\_insert\_comb.jpg).

OurBigBook likes Wikimedia Commons so much that we automatically parse the image URL and if it is from Wikimedia Commons, automatically deduce the `source` for you. So the above image renders the same without the `source` argument:
```
\Image[https://upload.wikimedia.org/wikipedia/commons/5/5b/Gel_electrophoresis_insert_comb.jpg]
```
which renders as:



> ![](https://upload.wikimedia.org/wikipedia/commons/5/5b/Gel_electrophoresis_insert_comb.jpg)
> 
> **[Figure 35](#_1408)** [Source](https://commons.wikimedia.org/wiki/File:Gel_electrophoresis_insert_comb.jpg).

And like for non-Wikimedia images, you can automatically generate a `title` from the `src` by setting the `titleFromSrc` [boolean argument](boolean-argument.md) or if `title-from-src` is set as the default [media provider](ourbigbook-json/media-providers.md) for the media type:
```
\Image[https://upload.wikimedia.org/wikipedia/commons/5/5b/Gel_electrophoresis_insert_comb.jpg]
{titleFromSrc}
```
which renders as:



> <a id="image-gel-electrophoresis-insert-comb"></a>
> ![](https://upload.wikimedia.org/wikipedia/commons/5/5b/Gel_electrophoresis_insert_comb.jpg)
> 
> **[Figure 36](#image-gel-electrophoresis-insert-comb). Gel electrophoresis insert comb.** [Source](https://commons.wikimedia.org/wiki/File:Gel_electrophoresis_insert_comb.jpg).

And a quick test for a more complex thumb resized URL:
```
\Image[https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Gel_electrophoresis_insert_comb.jpg/450px-Gel_electrophoresis_insert_comb.jpg]
```
which renders as:



> ![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Gel_electrophoresis_insert_comb.jpg/450px-Gel_electrophoresis_insert_comb.jpg)
> 
> **[Figure 37](#_1417)** [Source](https://commons.wikimedia.org/wiki/File:Gel_electrophoresis_insert_comb.jpg).

If you really absolutely want to turn off the `source`, you can explicitly set:
```
\Image[https://upload.wikimedia.org/wikipedia/commons/5/5b/Gel_electrophoresis_insert_comb.jpg]
{source=}
```
which renders as:



> ![](https://upload.wikimedia.org/wikipedia/commons/5/5b/Gel_electrophoresis_insert_comb.jpg)

but you don't want to do that for the most commonly Wikimedia Commons used license of CC BY+, do you? :-)

Upsides of using Wikimedia Commons for your images:
- makes it easier for other writers to find and reuse your images
- automatically generates resized versions of the uploaded images into several common dimensions so you can pick the smallest one that fits your desired [image height](image-height-argument.md) to reduce bandwidth usage
- if you have so many images that they would blow even the size of a [separate media repository](store-images-in-a-separate-media-repository.md), this will still work
Downsides:
- forces you to use the Creative Commons license
- requires the content to be educational in nature
- uploading a bunch of images to Wikimedia Commons does feel a bit more laborious than it should because you have to write down so much repeated metadata for them

## ↑ Ancestors (5)

1. [Where to store images](where-to-store-images.md)
2. [Image](image.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Video](video.md)
