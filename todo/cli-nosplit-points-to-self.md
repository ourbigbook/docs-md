# CLI nosplit points to self

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [CLI](cli.md), [Web upload](web-upload.md)

E.g.: [https://cirosantilli.com/education-level](https://cirosantilli.com/education-level) nosplit points to the page itself. Should instead point to [https://cirosantilli.com/education#education-level](https://cirosantilli.com/education#education-level)

Possiby happens only with:
```
  "publishOptions": {
    "toSplitHeaders": true,
    "htmlXExtension": false,
    "xPrefix": "https://ourbigbook.com/cirosantilli/"
  },
```
redirects enabled.

Further investigation shows that `"toSplitHeaders": true,` is the issue. Fixing this for now bu ust removing the split/nosplit in that case.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
