# Store images in a separate media repository

↑ **Parent:** [Where to store images](where-to-store-images.md)

In this approach, you create a separate GitHub repository in addition to the main one containing the text to contain only media such as images.

This approach is more suitable than [store images inside the repository itself](store-images-inside-the-repository-itself.md) if you are going to have a lot of images.

When using this approach, you could of course just point directly to the final image URL, e.g. as in:
```
\Image[https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/Fundamental_theorem_of_calculus_topic_page_arrow_to_full_article.png]
```
which renders as:



> ![](https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/Fundamental_theorem_of_calculus_topic_page_arrow_to_full_article.png)

but OurBigBook allows you use configurations that allow you to enter just the image basename: `Fundamental_theorem_of_calculus_topic_page_arrow_to_full_article.png` which we will cover next.

In order to get this to work, the recommended repository setup is:
- `./main-repo/.git`: main repository at [https://github.com/username/main-repo](https://github.com/username/main-repo)
- `./main-repo/data/media/.git/`: media repository at [https://github.com/username/main-repo-media](https://github.com/username/main-repo-media), and where `data/` is gitignored.
The directory and repository names are not mandatory, but if you place media in `data/media` and name its repository by adding the `*-media` suffix, then `ourbigbook` will handle everything for you without any further configuration in [`media-providers`](ourbigbook-json/media-providers.md).

This particular documentation repository does have a different setup as can be seen from its [ourbigbook.json](ourbigbook.json). Then, when everything is setup correctly, we can refer to images simply as:
```
\Image[Fundamental_theorem_of_calculus_topic_page_arrow_to_full_article.png]{provider=github}
```
which renders as:



> ![](https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/Fundamental_theorem_of_calculus_topic_page_arrow_to_full_article.png)

In this example, we also needed to set `{provider=github}` explicitly since it was not set as the default image provider in our `ourbigbook.json`. In most projects however, all of your images will be in the default repository, so this won't be needed.

`provider` must not be given when a full URL is given because we automatically detect providers from URLs, e.g.:
```
\Image[https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/Fundamental_theorem_of_calculus_topic_page.png]{provider=github}
```
is an error.

TODO implement: `ourbigbook` will even automatically add and push used images in the `my-tutorial-media` repository for you [during publishing](p-publish.md)!

You should then use the following rules inside `my-tutorial-media`:
- give every file a very descriptive and unique name as a full English sentence
- never ever delete any files, nor change their content, unless it is an improvement in format that does change the information contained of the image TODO link to nice Wikimedia Commons guideline page
This way, even though the repositories are not fully in sync, anyone who clones the latest version of the `*-media` directory will be able to view any version of the main repository.

Then, if one day the media repository ever blows up GitHub's limit, you can just migrate the images to another image server that allows arbitrary basenames, e.g. AWS, and just configure your project to use that new media base URL with the [`media-providers`](ourbigbook-json/media-providers.md) option.

The reason why images should be kept in a separate repository is that images are hundreds or thousands of times larger than hand written text.

Therefore, images could easily fill up the maximum repository size you are allowed: [https://webapps.stackexchange.com/questions/45254/file-size-and-storage-limits-on-github#84746](https://webapps.stackexchange.com/questions/45254/file-size-and-storage-limits-on-github#84746) and then what will you do when GitHub comes asking you to reduce the repository size?

[Git LFS](https://git-lfs.github.com/) is one approach to deal with this, but we feel that it adds too much development overhead.

**Table of contents**

- [Store images in a separate media repository and track it as a git submodule](store-images-in-a-separate-media-repository-and-track-it-as-a-git-submodule.md)

## ↑ Ancestors (5)

1. [Where to store images](where-to-store-images.md)
2. [Image](image.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (5)

- [Known URL protocols](known-url-protocols.md)
- [`Media-providers`](ourbigbook-json/media-providers.md)
- [Store images in Wikimedia Commons](store-images-in-wikimedia-commons.md)
- [Store images inside the repository itself](store-images-inside-the-repository-itself.md)
- [Video](video.md)
