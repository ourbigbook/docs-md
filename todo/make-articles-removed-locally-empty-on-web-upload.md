# Make articles removed locally empty on web upload

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Web](web.md), [Web upload](web-upload.md)

<a id="_483"></a>
Otherwise the following sequence leads to a hard to understand failure for the end user.

<a id="_484"></a>
First the user uploads with:

<a id="_485"></a>
```
== Header 1

== Header 2

\Image[img.png]{title=My image}
```

<a id="_486"></a>
Then, `Header 2` is completely removed from all source files and the image is moved to `Header 1`:

<a id="_487"></a>
```
== Header 1

\Image[img.png]{title=My image}
```

<a id="_488"></a>
Then, when the use tries to upload again, it fails because of duplicated id `image-my-image`.

<a id="_489"></a>
This above sequence of events is not ideal from the users' perspective, as a synonym generation would lead to better URLs:

<a id="_490"></a>
```
== Header 1

= Header 2
{synonym}

\Image[img.png]{title=My image}
```

<a id="_491"></a>
In that sequence, the File for `Header 2` would be effectively emptied of Ids, and there would be no duplicates.

<a id="_492"></a>
But still, if the user deletes a header, it becomes very difficult to know it later on. So perhaps when the CLI downloads the SHA list, it could also check if there are articles on server that both:<a id="_493"></a>

<a id="_494"></a>
- are not present locally anymore
<a id="_495"></a>
- have a non-empty hash
and then proceed to make any such headers empty to avoid ID duplication.

<a id="_496"></a>
Aditionaly, it would also be good to move the deleted articles to some predefined header to avoid cluttering the headers. E.g. we could start with a dummy "My deleted articles". Dedicated section: [Section "Move articles deleted locally to under a trash article on web"](move-articles-deleted-locally-to-under-a-trash-article-on-web.md).

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
