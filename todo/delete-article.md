# Delete article

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Web](web.md)

This is a bit hard to to properly as it requires checking that a billion dependant objects are also deleted:
- issues
- comments of those issues
- file
- IDs defined in that article
- change the parentId of all chidren to the parent article of the deleted article, and also updated nested set index
Some of those can go on cascades, but others will require side-effects.

Related:
- [https://github.com/ourbigbook/ourbigbook/issues/216](https://github.com/ourbigbook/ourbigbook/issues/216)

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
