# Store images inside the repository itself

↑ **Parent:** [Where to store images](where-to-store-images.md)

If you are making a limited repository that will not have a ton of images, then you can get away with simply git tracking your images in the main repository.

With this setup, no further action is needed. For example, with a file structure of:
```
./index.bigb
./Tank_man_standing_in_front_of_some_tanks.jpg
```
just use the image from `index.bigb` as:
```
\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
```
which renders as:



> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)

However, if you are making a huge tutorial, which can have a huge undefined number of images (i.e. any scientific book), then you likely don't want to git track your images in the git repository.

A generally better alternative is to [store images in a separate media repository](store-images-in-a-separate-media-repository.md), and especially [store images in a separate media repository and track it as a git submodule](store-images-in-a-separate-media-repository-and-track-it-as-a-git-submodule.md).

## ↑ Ancestors (5)

1. [Where to store images](where-to-store-images.md)
2. [Image](image.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [`Media-providers`](ourbigbook-json/media-providers.md)
- [Store images in a separate media repository](store-images-in-a-separate-media-repository.md)
- [Video](video.md)
