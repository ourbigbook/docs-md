<h1 id="-/file/web/bin/normalize">web/bin/normalize</h1>

↑ **Parent:** [Web CLI utils](../../../../web-cli-utils.md)

Check the counts of issues per article for user `barack-obama` only with `-c`, but don't fix anything:
```
web/bin/normalize -c -u barack-obama article-issue-count
```

Print the full correct normalized state with `-p`:
```
web/bin/normalize -f -u barack-obama issue-follower-count
```

Fix the counts of issue follower if any are wrong with `-f`, thus potentially altering the database:
```
web/bin/normalize -f -u barack-obama issue-follower-count
```

Backfill image dimensions for existing uploads after deploying the image-dimensions migration:
```
web/bin/normalize -f upload-image-dimensions
```
This processes one file at a time and preserves file bytes, hashes, and timestamps. Add `-u username` to limit it to one user. On Heroku, from the `web` directory:
```
./heroku run -- web/bin/normalize -f upload-image-dimensions
```
File previews use the metadata immediately. Existing article HTML needs a rerender, for example with `ourbigbook --web --web-force-render` after the backfill.

## ↑ Ancestors (6)

1. [Web CLI utils](../../../../web-cli-utils.md)
2. [OurBigBook Web directory structure](../../../../ourbigbook-web-directory-structure.md)
3. [OurBigBook Web architecture](../../../../ourbigbook-web-architecture.md)
4. [OurBigBook Web development](../../../../ourbigbook-web-development.md)
5. [OurBigBook Web](../../../../ourbigbook-web.md)
6. [OurBigBook Project](../../../../split.md)

## ← Incoming links (1)

- [OurBigBook Web database normalization](../../../../ourbigbook-web-database-normalization.md)
