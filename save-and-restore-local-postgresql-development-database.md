# Save and restore local PostgreSQL development database

↑ **Parent:** [OurBigBook Web PostgreSQL utils](ourbigbook-web-postgresql-utils.md)

Save the psql database state as per [https://stackoverflow.com/questions/37984733/postgresql-database-export-to-sql-file](https://stackoverflow.com/questions/37984733/postgresql-database-export-to-sql-file) with our [web/bin/pg_dump](web/bin/pg_dump) helper:
```
web/bin/pg_dump tmp.dump
```
Then to restore it later with [web/bin/pg_restore](web/bin/pg_restore):
```
web/bin/pg_restore tmp.dump
```
[https://stackoverflow.com/questions/2732474/restore-a-postgres-backup-file-using-the-command-line](https://stackoverflow.com/questions/2732474/restore-a-postgres-backup-file-using-the-command-line)

## ↑ Ancestors (5)

1. [OurBigBook Web PostgreSQL utils](ourbigbook-web-postgresql-utils.md)
2. [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Download Heroku database and restore it locally](download-heroku-database-and-restore-it-locally.md)
