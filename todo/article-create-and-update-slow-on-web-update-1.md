# Article create and update slow on web update 1

↑ **Parent:** [Article create and update slow on web](article-create-and-update-slow-on-web.md)

As of this commit did a bit further investigation with a better tooling and more understanding, notably now we run:
```
OURBIGBOOK_LOG_DB=1 num run dev-pg
```

Heroku is definitely slower than local, at around 1 t o2 s on the bit first ten pages:
```
ourbigbook --web --web-force-render --web-max-renders 10
```
but local was also rather slow when we have about the same number of articles for the user.

After some improved benchmarking setup, there seem to be two separate causes:
- preventing: `options.db_provider.fetch_header_tree_ids(` on web. It is not necessary as we render the ToC dynamically.

  This matters the most for toplevel articles with many descendants.
- the other problem we haven't solved yet: the nested index update querries are slow. We don't know how to solve that easily.

  Those querries simply update a huge number of rows.

  Maybe we could have a fallback mechanism to build that index on the background, and use the tree index temporarily?

  Hard call.

## ↑ Ancestors (4)

1. [Article create and update slow on web](article-create-and-update-slow-on-web.md)
2. [Closed issues](closed-issues.md)
3. [TODO](../todo-split.md)
4. [OurBigBook Project](../split.md)
