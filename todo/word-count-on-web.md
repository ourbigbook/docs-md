# Word count on web

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Web](web.md), [Word count](word-count.md)

Likely also at same time do a source character count.

Likely would be easy to implement as it would reuse the exact same query that we already use to update ncestors of the nested set index.

Was removed at: [remove word count on web](remove-word-count-on-web.md) because would require actually implementing properly but lazy.

We should likely not show it on link hover however, only headers, as doing so would mean having to update every single page that links to a header for correctness. If this is ever done, it should be Js runtime stuff only.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Remove word count on web](remove-word-count-on-web.md)
