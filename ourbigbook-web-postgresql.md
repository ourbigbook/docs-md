# OurBigBook Web PostgreSQL

↑ **Parent:** [OurBigBook Web development](ourbigbook-web-development.md)

PostgreSQL is the database that we use on production, and sometimes is is necessary to test stuff with it locally.

There are two main types of run with PostgreSQL:
- [Local run as identical to deployment as possible](local-run-as-identical-to-deployment-as-possible.md): uses PostgreSQL, but also sets as much as possible to match production, including Next.js rendering stuff
- [Local development run with PostgreSQL](local-development-run-with-postgresql.md): uses PostgreSQL database, but keeps everything else in development mode

To interactively inspect the local development database use our helper at [web/bin/psql](web/bin/psql):
```
web/bin/psql
```
Commands can be run as usual:
```
web/bin/psql -c 'SELECT * FROM "Article";'
```
It uses `PGPASSWORD` is mentioned at: [https://stackoverflow.com/questions/6405127/how-do-i-specify-a-password-to-psql-non-interactively](https://stackoverflow.com/questions/6405127/how-do-i-specify-a-password-to-psql-non-interactively)

**Table of contents**

- [OurBigBook Web PostgreSQL setup](ourbigbook-web-postgresql-setup.md)
- [Local run as identical to deployment as possible](local-run-as-identical-to-deployment-as-possible.md)
- [Local development run with PostgreSQL](local-development-run-with-postgresql.md)
- [Use a secondary PostgresQL database locally](use-a-secondary-postgresql-database-locally.md)
- [OurBigBook Web PostgreSQL utils](ourbigbook-web-postgresql-utils.md)
  - [web/bin/pg-kill-queries](_file/web/bin/pg-kill-queries.md)
  - [Save and restore local PostgreSQL development database](save-and-restore-local-postgresql-development-database.md)
  - [web/bin/psql](_file/web/bin/psql.md)
  - [web/bin/pg-ls-queries](_file/web/bin/pg-ls-queries.md)

## 🏷️ Tagged (1)

- [Web searches find words inside title on PostgreSQL](news/web-searches-find-words-inside-title-on-postgresql.md)

## ↑ Ancestors (3)

1. [OurBigBook Web development](ourbigbook-web-development.md)
2. [OurBigBook Web](ourbigbook-web.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Web searches find words inside title on PostgreSQL](news/web-searches-find-words-inside-title-on-postgresql.md)
- [OurBigBook Web analytics](ourbigbook-web-analytics.md)
