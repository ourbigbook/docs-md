# test-migration

↑ **Parent:** [OurBigBook Web database migration setup](ourbigbook-web-database-migration-setup.md)

Since sequelize migrations are so hard to get right, it is fundamental to test them.

One way to do it is with our [web/bin/test-migration](web/bin/test-migration) script:
```
cd web
bin/test-migration -u1 -a3
```
For PostgresQL:
```
bin/pg bin/test-migration -u1 -a3
```
Note that Sequelize SQLite migrations are basically worthless and often incorrectly fail due to foreign key constraints: [https://stackoverflow.com/questions/62667269/sequelize-js-how-do-we-change-column-type-in-migration/70486686#70486686](https://stackoverflow.com/questions/62667269/sequelize-js-how-do-we-change-column-type-in-migration/70486686#70486686) so you might not care much about making them pass and focus only PostgreSQL.

The `test-migration` script:
- does a git checkout out to the previous commit
- regenerates the database
- checks out to master
- and then does the migration

The arguments of `test-migration` are fowarded to [web/bin/generate-demo-data.js](web/bin/generate-demo-data.js) from [demo data](demo-data.md), `-u1 -a5` would produce a small ammount of data, suitable for quick iteration tests.

Towards the end of that script, we can see lines of type:
```
+ diff -u tmp.old.sqlite3.sort.sql tmp.new-clean.sqlite3.sort.sql
+ diff -u tmp.new-clean.sqlite3.sort.sql tmp.new-migration.sqlite3.sort.sql
```
Those are important diffs you might want to look at every time:
- `tmp.old.sqlite3.sort.sql`: old schema before migration, but with lines sorted alphabetically
- `tmp.new-clean.sqlite3.sort.sql`: new schema achieved by dropping the database and re creating at once
- `tmp.new-migration.sqlite3.sort.sql`: new schema achieved migrating from the old state
Therefore, you really want the `diff tmp.old.sqlite3.schema tmp.new-clean.sqlite3.schema` to be empty. For sqlite3 we actually check that and give an error if they differ, but for PostgreSQL it is a bit harder due to the multiline statements, so just inspect the diffs manually.

## ↑ Ancestors (6)

1. [OurBigBook Web database migration setup](ourbigbook-web-database-migration-setup.md)
2. [OurBigBook Web database](ourbigbook-web-database.md)
3. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
4. [OurBigBook Web development](ourbigbook-web-development.md)
5. [OurBigBook Web](ourbigbook-web.md)
6. [OurBigBook Project](split.md)
