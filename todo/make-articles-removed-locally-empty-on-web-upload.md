# Make articles removed locally empty on web upload

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Web](web.md), [Web upload](web-upload.md)

Otherwise the following sequence leads to a hard to understand failure for the end user.

First the user uploads with:

```
== Header 1

== Header 2

\Image[img.png]{title=My image}
```

Then, `Header 2` is completely removed from all source files and the image is moved to `Header 1`:

```
== Header 1

\Image[img.png]{title=My image}
```

Then, when the use tries to upload again, it fails because of duplicated id `image-my-image`.

This above sequence of events is not ideal from the users' perspective, as a synonym generation would lead to better URLs:

```
== Header 1

= Header 2
{synonym}

\Image[img.png]{title=My image}
```

In that sequence, the File for `Header 2` would be effectively emptied of Ids, and there would be no duplicates.

But still, if the user deletes a header, it becomes very difficult to know it later on. So perhaps when the CLI downloads the SHA list, it could also check if there are articles on server that both:
- are not present locally anymore
- have a non-empty hash
and then proceed to make any such headers empty to avoid ID duplication.

Aditionaly, it would also be good to move the deleted articles to some predefined header to avoid cluttering the headers. E.g. we could start with a dummy "My deleted articles". Dedicated section: [Section "Move articles deleted locally to under a trash article on web"](move-articles-deleted-locally-to-under-a-trash-article-on-web.md).

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
