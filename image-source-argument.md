# Image `source` argument

↑ **Parent:** [Image argument](image-argument.md)  
🏷️ **Tags:** [Named argument](named-argument.md)

Where the image was taken from, e.g.:
```
\Image[https://upload.wikimedia.org/wikipedia/commons/6/68/Akha_cropped_hires.JPG]
{title=A couple}
{source=https://en.wikipedia.org/wiki/Human}
```
which renders as:



> <a id="image-a-couple"></a>
> ![](https://upload.wikimedia.org/wikipedia/commons/6/68/Akha_cropped_hires.JPG)
> 
> **[Figure 42](#image-a-couple). A couple**. [Source](https://en.wikipedia.org/wiki/Human).

The `source` is automatically inferred for certain known websites, e.g.:
- Wikimedia `https://upload.wikimedia.org/wikipedia/commons`
  - from: [https://upload.wikimedia.org/wikipedia/commons/6/68/Akha_cropped_hires.JPG](https://upload.wikimedia.org/wikipedia/commons/6/68/Akha_cropped_hires.JPG)
  - to: [https://en.wikipedia.org/wiki/File:Akha_cropped_hires.JPG](https://en.wikipedia.org/wiki/File:Akha_cropped_hires.JPG)

  Example:
  ```
  \Image[https://upload.wikimedia.org/wikipedia/commons/6/68/Akha_cropped_hires.JPG]
  {title=A couple no source}
  ```

  which renders as:

  > <a id="image-a-couple-no-source"></a>
  > ![](https://upload.wikimedia.org/wikipedia/commons/6/68/Akha_cropped_hires.JPG)
  > 
  > **[Figure 43](#image-a-couple-no-source). A couple no source**. [Source](https://commons.wikimedia.org/wiki/File:Akha_cropped_hires.JPG).

## ↑ Ancestors (5)

1. [Image argument](image-argument.md)
2. [Image](image.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Image](image.md)
