# OurBigBook Web run unit tests in PostgreSQL

↑ **Parent:** [OurBigBook Web unit tests](ourbigbook-web-unit-tests.md)

To run the tests on PostgreSQL instead of the default SQLite, first setup the test database analogously to [local run as identical to deployment as possible](local-run-as-identical-to-deployment-as-possible.md):
```
cd web
bin/pg-setup ourbigbook_test
```
and then run with:
```
npm run test-pg
```
Run only matching tests on PostgreSQL:
```
npm run test-pg -- -g 'substring of test title'
```

Running tests erases all data present in the database used. In order to point to a custom database use:
```
DATABASE_URL_TEST=postgres://realworld_next_user:a@localhost:5432/realworld_next_test npm run test-pg
```
We don't use `DATABASE_URL` when running tests as a safeguard to reduce the likelihood of accidentally nuking the production database.

The test database contains the state of the latest test run at the end of the run. You can inspect it with [web/bin/psql](_file/web/bin/psql.md) with:
```
bin/psql -d ourbigbook_test
```

## ↑ Ancestors (4)

1. [OurBigBook Web unit tests](ourbigbook-web-unit-tests.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [web/bin/psql](_file/web/bin/psql.md)
