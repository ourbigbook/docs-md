# Use a secondary PostgresQL database locally

↑ **Parent:** [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)

Setup the database:
```
web/bin/pg-setup ourbigbook2
OURBIGBOOK_DB_NAME=ourbigbook2 web/bin/pg web/bin/generate-demo-data.js
```

Run the server:
```
OURBIGBOOK_DB_NAME=ourbigbook2 npm run dev-pg
```

Or commonly to run on a different port so that two instances may be accessed separately:
```
PORT=3001 OURBIGBOOK_DB_NAME=ourbigbook2 npm run dev-pg
```

To restore a dump to the secondary database:
```
web/bin/pg_restore -d ourbigbook2 latest.dump
```

## ↑ Ancestors (4)

1. [OurBigBook Web PostgreSQL](ourbigbook-web-postgresql.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
