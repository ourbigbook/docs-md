# iframe macro

↑ **Parent:** [Issues](issues.md)

Reasonable results can already be obtained with:  
\<iframe src="-/raw/js/matterjs/examples.html\#top-down-asdw-fixed-viewport" width="1000" height="850"\>\</iframe\>  
The main issue with that is the possibly changing `-/raw/js/matterjs/examples.html` path depending on scopes, and it is also not very nice to have to write `-/raw` explicitly.

Instead we should do the same handling as is currently done for `\a[]` and `\Image[]` on these paths.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
