# Demo data

↑ **Parent:** [Generated data](generated-data.md)

You can generate demo data for [OurBigBook Web](ourbigbook-web.md) with [web/bin/generate-demo-data.js](web/bin/generate-demo-data.js), e.g.:
```
cd web
./bin/generate-demo-data --users 2 --articles-per-user 10
```

Every time this is run, it tries to update existing entities such as users and articles first, and only creates them if they don't exist. This allows us to update all demo data on a live website that also has users without deleting any user data.

Note however that if you ever increase the ammount of demo users, you might overwrite real user data. E.g. if you first do:
```
./bin/generate-demo-data --users 2 --articles-per-user 10
```
and then some time later:
```
./bin/generate-demo-data --users 4 --articles-per-user 10
```
it is possible that some real user will have taken up the username that we use for the third user, which did not exist previously, and then hacks their articles away. So never ever do that! Just stick to the default values in production.

As a safeguard, to be able to run this in production you have to also pass the `--force-production` flag;
```
./bin/generate-demo-data --users 2 --articles-per-user 10 --force-production
```

To first fully clear the database, including any real user data, before doing anything else, use `--clear`, e.g.:
```
./bin/generate-demo-data --users 4 --articles-per-user 10 --clear
```

To clear the database and start with an empty database use `--empty`:
```
./bin/generate-demo-data --empty
```

To regenerate the PostgreSQL database instead of SQLite as mentioned at [local development run with PostgreSQL](local-development-run-with-postgresql.md):
```
OURBIGBOOK_POSTGRES=1 ./bin/generate-demo-data.js
```

**Table of contents**

- [Demo data local file output](demo-data-local-file-output.md)

## ↑ Ancestors (4)

1. [Generated data](generated-data.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [Heroku deployment](heroku-deployment.md)
- [Local development server](local-development-server.md)
- [OurBigBook Web database migration setup](ourbigbook-web-database-migration-setup.md)
- [test-migration](test-migration.md)
