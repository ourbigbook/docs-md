# Fix parentId and previousSiblingId on articles API

↑ **Parent:** [Issues](issues.md)

The underlying reason is that:
```
.getArticles({includeParentAndPreviousSibling: true
```
is broken. The singular version `getArticle` however is not.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
