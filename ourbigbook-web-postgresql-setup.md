# OurBigBook Web PostgreSQL setup

↑ **Parent:** [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)

Before running [OurBigBook Web](ourbigbook-web.md), the PostgreSQL database should be setup with [web/bin/pg-setup](web/bin/pg-setup):
```
web/bin/pg-setup
```
This command:
- drops the existing database if any, i.e. nukes all data
- creates a test user
- re-creates the test database

## ↑ Ancestors (4)

1. [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Heroku deployment](heroku-deployment.md)
- [Local run as identical to deployment as possible](local-run-as-identical-to-deployment-as-possible.md)
