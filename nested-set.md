# Nested set

↑ **Parent:** [OurBigBook Web database](ourbigbook-web-database.md)

The "nested set index" is an index explicitly maintained by our codebase that allows quickly fetching pages for [OurBigBook Web dynamic article tree](ourbigbook-web-dynamic-article-tree.md) in [pre-order depth first](https://ourbigbook.com/go/topic/pre-order-depth-first), i.e. the conventional order in which  the table of contents and articlees appear in a book. See also: [https://stackoverflow.com/questions/4048151/what-are-the-options-for-storing-hierarchical-data-in-a-relational-database](https://stackoverflow.com/questions/4048151/what-are-the-options-for-storing-hierarchical-data-in-a-relational-database)

This technique is also called "closure table" by some authors.

This index is, as the name indicates, an index, i.e. it duplicates information otherwise present in the [OurBigBook Web `Ref` database table](ourbigbook-web-ref-database-table.md), which contains an adjacency list format instead, in the hope that it would be faster to pre-order depth first traverse.

This feature adds considerable complexity to the codebase. Also, updates can be considerably slow, as updating this index for a single article requires updating the index value for most or all other articles as well. We should bechmark it better vs recursive queries.

This index was partly introduced as a helper rather than as a pure speed up, as it is a bit hard to do pre order tree traversal in SQLite due to the lack of arrays. In PostgreSQL we can do it well: [https://stackoverflow.com/questions/65247873/preorder-tree-traversal-using-recursive-ctes-in-sql/77276675#77276675](https://stackoverflow.com/questions/65247873/preorder-tree-traversal-using-recursive-ctes-in-sql/77276675#77276675)

## ↑ Ancestors (5)

1. [OurBigBook Web database](ourbigbook-web-database.md)
2. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (5)

- [`--no-web-nested-set-bulk`](no-web-nested-set-bulk.md)
- [OurBigBook Web database normalization](ourbigbook-web-database-normalization.md)
- [OurBigBook Web dynamic article tree](ourbigbook-web-dynamic-article-tree.md)
- [`--web-nested-set` (option)](web-nested-set-option.md)
- [Wikipedia bot](wikipedia-bot.md)
