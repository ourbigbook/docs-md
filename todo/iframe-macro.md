# iframe macro

↑ **Parent:** [Cannot link from comment to article](cannot-link-from-comment-to-article.md)

<a id="_379"></a>
Reasonable results can already be obtained with:  
\<iframe src="\_raw/js/matterjs/examples.html\#top-down-asdw-fixed-viewport" width="1000" height="850"\>\</iframe\>  
The main issue with that is the possibly changing `_raw/js/matterjs/examples.html` path depending on scopes, and it is also not very nice to have to write `_raw` explicitly.

<a id="_380"></a>
Instead we should do the same handling as is currently done for `\a[]` and `\Image[]` on these paths.

## ↑ Ancestors (3)

1. [Cannot link from comment to article](cannot-link-from-comment-to-article.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
