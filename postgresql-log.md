# PostgreSQL log

↑ **Parent:** [Log database queries](log-database-queries.md)

It might be wise to enable PostgreSQL query logging by default with: `log_statement` for development. TODO does it noticeably affect performance?

See: [https://stackoverflow.com/questions/722221/how-to-log-postgresql-queries](https://stackoverflow.com/questions/722221/how-to-log-postgresql-queries)

One major advantage of this method is that Sequelize's error logging is a bit crap, and sometimes the error appears much much more clearly in the PostgreSQL logs.

## ↑ Ancestors (4)

1. [Log database queries](log-database-queries.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
