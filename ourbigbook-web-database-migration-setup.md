# OurBigBook Web database migration setup

↑ **Parent:** [OurBigBook Web database](ourbigbook-web-database.md)

Any pending migrations are done automatically during deployment as part of `npm run build`, more precisely they are run from [web/bin/sync-db.js](web/bin/sync-db.js).

We also have a custom setup where, if the database is not initialized, we first:
- just creates the database from the latest model descriptions
- manually fill in the `SequelizeMeta` migration tracking table with all available migrations to tell Sequelize that all migrations have been done up to this point
This is something that should be merged into Sequelize itself, or at least asked on Stack Overflow, but lazy now.

In order to test migrations locally interactively, you can:
- commit them on Git
- `git checkout HEAD~`
- reset the database with [demo data](demo-data.md):
  ```
  cd web
  ./bin/generate-demo-data.js --clear
  ```
- Move back to master:  
  `git checkout -`
- Run the migration:
  ```
  ./bin/sync-db.js
  ```

**Table of contents**

- [test-migration](test-migration.md)
- [OurBigBook Web nuke DB instead of migrating](ourbigbook-web-nuke-db-instead-of-migrating.md)

## ↑ Ancestors (5)

1. [OurBigBook Web database](ourbigbook-web-database.md)
2. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [web/bin/rerender-articles.js](_file/web/bin/rerender-articles.js.md)
- [Local development run with PostgreSQL](local-development-run-with-postgresql.md)
- [OurBigBook Web directory structure](ourbigbook-web-directory-structure.md)
