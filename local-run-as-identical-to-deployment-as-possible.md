# Local run as identical to deployment as possible

↑ **Parent:** [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)

Here we use PostgreSQL instead of SQLite with the prebuilt static frontend.

For when you really need to debug some deployment stuff locally.

Before the first run, do the [OurBigBook Web PostgreSQL setup](ourbigbook-web-postgresql-setup.md).

Then, after every modification
```
npm run build-prod
npm run start-prod
```
and then visit the running website at: [http://localhost:3000/](http://localhost:3000/)

To optionally nuke the database and create the demo data:
```
npm run seed-prod
```
or alternatively to start from a clean database:
```
psql -c "DROP DATABASE ourbigbook"
createdb ourbigbook
psql -c 'GRANT ALL PRIVILEGES ON DATABASE ourbigbook TO ourbigbook_user'
```

You can inspect the database interactively with:
```
psql ourbigbook
```
and then running SQL commands.

## ↑ Ancestors (4)

1. [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (5)

- [Local development run with PostgreSQL](local-development-run-with-postgresql.md)
- [Local optimized frontend](local-optimized-frontend.md)
- [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)
- [OurBigBook Web run unit tests in PostgreSQL](ourbigbook-web-run-unit-tests-in-postgresql.md)
- [Test system](test-system.md)
