<h1 id="check-db-only"><code>--check-db-only</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Check the database for consistency, e.g. duplicated IDs. Don't do anything else, including [ID extraction](id-extraction.md), which must have been done previously.

Normal full-directory builds cache successful database checks in the local SQLite database. The CLI logs each file as it is checked and stops at the first failure. Successfully checked files remain cached even if a later file fails, so rerunning reaches the failing file faster; the failing file's reference changes are rolled back and unchecked files are not marked successful. Text and link edits recheck the changed files, while changes to available IDs, synonyms, the parent tree, configuration or checker code invalidate the broader cache. Media-file existence and cross-file duplicate tags are still checked for cached files. This also applies to the local preparation of [`-W`, `--web`](web.md) uploads, not the server-side build jobs. Use `--check-db-only` to force a complete database check without using the cache.

The initial use case was for usage in [Parallel builds](jobs.md).

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`-j`, `--jobs <n>`](jobs.md)
- [`--no-check-db`](no-check-db.md)
