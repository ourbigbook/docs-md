# OurBigBook Web unit tests

↑ **Parent:** [OurBigBook Web development](ourbigbook-web-development.md)

All our tests are all located inside [test.js](test.js).

They can be run with:
```
cd web
npm test
```

The dynamic website tests also uses Mocha just like [the tests for OurBigBook CLI and OurBigBook Library](test-system.md), so similar usage patterns apply, e.g. to run just a single test:
```
npm test -- -g 'substring of test title'
```
or to show database queries being done in the tests:
```
DEBUG='*:sql:*' npm test
```

The tests include two broad classes of tests:
- API tests: launch the server on a random port, and run API commands, thus testing the entire backend
- smaller unit tests that only call certain functions directly
- TODO: create frontend tests: [https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app/issues/11](https://github.com/cirosantilli/node-express-sequelize-nextjs-realworld-example-app/issues/11)

**Table of contents**

- [OurBigBook Web run unit tests in PostgreSQL](ourbigbook-web-run-unit-tests-in-postgresql.md)
- [OurBigBook Web Next.js unit tests](ourbigbook-web-next-js-unit-tests.md)

## ↑ Ancestors (3)

1. [OurBigBook Web development](ourbigbook-web-development.md)
2. [OurBigBook Web](ourbigbook-web.md)
3. [OurBigBook Project](split.md)
