# `(beta)` on navbar gets pushed down half way at a specific page width just above mobile shift

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [CSS](css.md), [Web](web.md)

Just keep making viewport smaller an smaller, until it happen. Sample width that reproduces: 680px.

Removing `white-space: pre-wrap` solves it. But then the space between `(beta)` and `OurBigBook.com` gets removed.

OK: found out I had already previously solved the same issue with `&nbsp;`, redoing the "hack". Every header space has to be `&nbsp;`.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
