<h1 id="store-sha-of-each-article-plus-descendants-and-skip-api-re-renders-for-entire-subtrees">Store SHA of each article + descendants and skip API re-renders for entire subtrees</h1>

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Web](web.md), [Web upload](web-upload.md)

<a id="_211"></a>
This is one step beyond [skip re-render from API if article was unchanged](skip-re-render-from-api-if-article-was-unchanged.md) as it removes the requirement of actually uploading thousands of lines of content.

<a id="_212"></a>
It requires negotiating with the server instead.

<a id="_213"></a>
This would be particularly powerful if we included the descendants on the SHA of each parent, much like Git. This way we could skip enter unmodified subtrees, likely like Git.

<a id="_214"></a>
Yes, we are somewhat re-implementing parts of Git with this. But at least it is simple, and works at a sub-blob level given our grater specialization to our specific use case.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [`-W`, `--web`](../web.md)
