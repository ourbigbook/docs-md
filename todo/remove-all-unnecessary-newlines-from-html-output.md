# Remove all unnecessary newlines from HTML output

↑ **Parent:** [Cannot link from comment to article](cannot-link-from-comment-to-article.md)  
🏷️ **Tags:** [Lib](lib.md)

<a id="_352"></a>
These newlines were added for debugging purposes, but debugging should just be done with:<a id="_353"></a>

```
npx js-beautify min.html
```

<a id="_354"></a>
Newlines just add complexity to our codebase, and are not even getting removed from final output as things stand to take up a little bit of useless space.

## ↑ Ancestors (3)

1. [Cannot link from comment to article](cannot-link-from-comment-to-article.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
