<h1 id="_file/web/bin/psql">web/bin/psql</h1>

↑ **Parent:** [OurBigBook Web PostgreSQL utils](../../../ourbigbook-web-postgresql-utils.md)

Helper that gives  `psql` PostgreSQL shell on the default database (`ourbigbook`).

To select another database use the `-d` option: E.g. to use the `ourbigbook_test` database from [OurBigBook Web run unit tests in PostgreSQL](../../../ourbigbook-web-run-unit-tests-in-postgresql.md):
```
bin/psql -d ourbigbook_test
```

`psql` just forwards everything to the underlying `psql` command, so you can e.g. run a SQL script stored in a file with:
```
bin/psql <tmp.sql
```
or run an SQL query from CLI with:
```
bin/psql -c 'select * from "Id"'
```

## ↑ Ancestors (5)

1. [OurBigBook Web PostgreSQL utils](../../../ourbigbook-web-postgresql-utils.md)
2. [OurBigBook Web PostgreSQL](../../../ourbigbook-web-postgresql.md)
3. [OurBigBook Web development](../../../ourbigbook-web-development.md)
4. [OurBigBook Web](../../../ourbigbook-web.md)
5. [OurBigBook Project](../../../split.md)

## ← Incoming links (1)

- [OurBigBook Web run unit tests in PostgreSQL](../../../ourbigbook-web-run-unit-tests-in-postgresql.md)
