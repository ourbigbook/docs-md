# Load more articles

↑ **Parent:** [Cannot link from comment to article](cannot-link-from-comment-to-article.md)  
🏷️ **Tags:** [Dynamic tree fetch](dynamic-tree-fetch.md), [Web](web.md)

<a id="_362"></a>
Either with scroll or a load more button. Slightly tempted by a load more button?

<a id="_363"></a>
To implement, we just have to expose the ArticlePage.ts fetch in an API manner. The page then tracks current limit on a state variable, and just requests more from that point onwards.

<a id="_364"></a>
Starting from the commit of this line, we are also going to limit the ToC, so a load more button on ToC would also be of interest: [load more ToC entrie](load-more-toc-entrie.md).

## ↑ Ancestors (3)

1. [Cannot link from comment to article](cannot-link-from-comment-to-article.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [OurBigBook Web dynamic article tree](../ourbigbook-web-dynamic-article-tree.md)
