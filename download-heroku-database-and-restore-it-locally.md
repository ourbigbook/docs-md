# Download Heroku database and restore it locally

↑ **Parent:** [Heroku debugging](heroku-debugging.md)

First download a dump of the database as per [https://devcenter.heroku.com/articles/heroku-postgres-import-export](https://devcenter.heroku.com/articles/heroku-postgres-import-export) with [web/bin/pg_dump_heroku](web/bin/pg_dump_heroku):
```
web/bin/pg_dump_heroku
```
This produces a file `latest.dump` with the database dump. If that already exists, it gets overwritten.

Restoring that database locally to reproduce bugs can be done with the helper [web/bin/pg_restore_heroku_local](web/bin/pg_restore_heroku_local):
```
web/bin/pg_restore_heroku_local
```

Restoring that local database dump to Heroku when reverting back isuses can be done with the helper [web/bin/pg_restore_heroku_remote](web/bin/pg_restore_heroku_remote):
```
web/bin/pg_restore_heroku_remote
```
This will then ask you to type an interactive confirmation which we have not disabled by default.

That helper restore the local `latest.dump` database file like in [Section "Save and restore local PostgreSQL development database"](save-and-restore-local-postgresql-development-database.md). First we nuke the database completely with [web/bin/pg-setup](web/bin/pg-setup) to increase accuracy:
```
web/bin/pg-setup
web/bin/pg_restore --no-acl --no-owner latest.dump
```
We also add some extra flags to reduce the ammount of warnings and errors due to database differences. The command does not exit with status 0. [https://devcenter.heroku.com/articles/heroku-postgres-import-export](https://devcenter.heroku.com/articles/heroku-postgres-import-export) says some of those warnings are normal and can be ignored.

## ↑ Ancestors (6)

1. [Heroku debugging](heroku-debugging.md)
2. [Heroku deployment](heroku-deployment.md)
3. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
4. [OurBigBook Web development](ourbigbook-web-development.md)
5. [OurBigBook Web](ourbigbook-web.md)
6. [OurBigBook Project](split.md)
