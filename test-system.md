# Test system

↑ **Parent:** [Developing OurBigBook](developing-ourbigbook.md)

Run all tests:
```
npm test
```

To run all tests on PostgreSQL as in the [OurBigBook Web](ourbigbook-web.md), first setup the PostgreSQL database similarly to [local run as identical to deployment as possible](local-run-as-identical-to-deployment-as-possible.md):
```
createdb ourbigbook_cli
psql -c "CREATE ROLE ourbigbook_user with login password 'a'"
psql -c 'GRANT ALL PRIVILEGES ON DATABASE ourbigbook_cli TO ourbigbook_user'
psql -c 'GRANT ALL ON SCHEMA public TO ourbigbook_user'
psql -c 'GRANT USAGE ON SCHEMA public TO ourbigbook_user'
psql -c 'ALTER DATABASE ourbigbook_cli OWNER TO ourbigbook_user'
```
This got really annoying with PostgreSQL 15: [https://stackoverflow.com/questions/67276391/why-am-i-getting-a-permission-denied-error-for-schema-public-on-pgadmin-4](https://stackoverflow.com/questions/67276391/why-am-i-getting-a-permission-denied-error-for-schema-public-on-pgadmin-4) And then run with:
```
npm run test-pg
```

List all tests:
```
node node_modules/mocha-list-tests/mocha-list-tests.js main.js
```
as per: [https://stackoverflow.com/questions/41380137/list-all-mocha-tests-without-executing-them/58573986#58573986](https://stackoverflow.com/questions/41380137/list-all-mocha-tests-without-executing-them/58573986#58573986).

Run just one test by name:
```
npm test -- -g 'one paragraph'
```
or on PostgreSQL:
```
npm run test-pg -- -g 'one paragraph'
```
As per: [https://stackoverflow.com/questions/10832031/how-to-run-a-single-test-with-mocha](https://stackoverflow.com/questions/10832031/how-to-run-a-single-test-with-mocha) todo: what if the test name is a substring? You will want these Bash aliases:
```
npmtg() ( npm test -- -g "$*" )
npmtpg() ( npm run test-pg -- -g "$*" )
```
which allos you to just:
```
npmtg one paragraph
npmtpg one paragraph
```

Run all tests that don't start with `cli:`:
```
npm test -- -g '^(?!cli:)'
```
This works because `-g` takes JavaScript regular expressions, so we can use negative lookahead, see also: [https://stackoverflow.com/questions/26908288/with-mocha-how-do-i-run-all-tests-that-dont-have-slow-in-the-name](https://stackoverflow.com/questions/26908288/with-mocha-how-do-i-run-all-tests-that-dont-have-slow-in-the-name)

**Table of contents**

- [Inspect the database after a test](inspect-the-database-after-a-test.md)
- [Step debug when running a test](step-debug-when-running-a-test.md)
- [`lib:` vs `cli:` tests](lib-vs-cli-tests.md)

## ↑ Ancestors (2)

1. [Developing OurBigBook](developing-ourbigbook.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [Do the release](do-the-release.md)
- [OurBigBook Web Next.js unit tests](ourbigbook-web-next-js-unit-tests.md)
- [OurBigBook Web unit tests](ourbigbook-web-unit-tests.md)
- [Overview of files in this repository](overview-of-files-in-this-repository.md)
