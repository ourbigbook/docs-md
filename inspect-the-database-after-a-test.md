# Inspect the database after a test

↑ **Parent:** [Test system](test-system.md)

Suppose you selected a single test:
```
npm test -- -g 'cli: empty document'
```
and want to inspect the [ID database](cross-file-internal-link-internals.md) database status.

On SQLite it is not currently possible as tests run on a temporary in-memory database. TODO create a way.

On PostgreSQL, you can just inspect the `ourbigbook_cli` table with the `psql` command line executable, e.g..
```
psql ourbigbook_cli -c 'select * from "Id"'
```
That table is used to run each test, and will contain the contents of the last test executed.

## ↑ Ancestors (3)

1. [Test system](test-system.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)
