# Add an option to add a prefix to every ID of rendered output to avoid conflicts across comments and issue

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Comment](comment.md), [Web](web.md)

<a id="_667"></a>
[https://github.com/ourbigbook/ourbigbook/issues/251](https://github.com/ourbigbook/ourbigbook/issues/251)

<a id="_668"></a>
We noticed this is hard to implement, because we want internal links to still work, and just adding a prefix to every ID does not take that into account.

<a id="_669"></a>
We later noticed that what we actually want to solve the comment use case, is a custom toplevel scope, which we can easily implement with a custom named directory. So... scopes save the day for once?

<a id="_670"></a>
Will be useful for comments on web, since a single author can make multiple comments, so prefixing by usernme won't be enough.

<a id="_671"></a>
For topic pages, we can just prefix by username, and that is already currently done.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
