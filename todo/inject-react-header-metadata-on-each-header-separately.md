# Inject React header metadata on each header separately

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Web](web.md)

This is closely related to: [Reach the same performance as static website with dynamic tree](reach-the-same-performance-as-static-website-with-dynamic-tree.md). Performance considerations should guide if we actually want this or not.

No more need for:
```
for (const h of elem.querySelectorAll('.h')) {
```
on `Article.tsx` now that we have separate headers, we can just inject it one by one.

Bibliography:

- [https://stackoverflow.com/questions/44643424/how-to-parse-html-to-react-component](https://stackoverflow.com/questions/44643424/how-to-parse-html-to-react-component)
- [https://stackoverflow.com/questions/36104302/how-do-i-convert-a-string-to-jsx](https://stackoverflow.com/questions/36104302/how-do-i-convert-a-string-to-jsx)
- [https://stackoverflow.com/questions/71224517/is-it-possible-to-inject-a-next-js-component-into-an-existing-application-html](https://stackoverflow.com/questions/71224517/is-it-possible-to-inject-a-next-js-component-into-an-existing-application-html)

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
