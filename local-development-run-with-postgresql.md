# Local development run with PostgreSQL

↑ **Parent:** [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)

If you have determined that a bug is PostgreSQL specific, and it is easier to debug it interactively, first create the database as mentioned at [local run as identical to deployment as possible](local-run-as-identical-to-deployment-as-possible.md) and then:
```
OURBIGBOOK_POSTGRES=1 ./bin/generate-demo-data.js
OURBIGBOOK_POSTGRES=1 npm run dev
```
or shortcut for the run:
```
npm run dev-pg
```

Note that doing `sync-db` also requires `NODE_ENV=production` as in:
```
NODE_ENV=production OURBIGBOOK_POSTGRES=1 bin/sync-db.js
```
because we have to shell out to the ugly [migration](ourbigbook-web-database-migration-setup.md) CLI, and that only understands `NODE_ENV`.

## ↑ Ancestors (4)

1. [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Demo data](demo-data.md)
- [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)
