# Log specific database queries

↑ **Parent:** [Log database queries](log-database-queries.md)

However, you often want to long only a few selected queries, otherwise it becomes very difficult to determine which query is which, in particular due asynchronous execution. In this case, use the technique mentioned at: [https://stackoverflow.com/questions/21427501/how-can-i-see-the-sql-generated-by-sequelize-js/21431627#21431627](https://stackoverflow.com/questions/21427501/how-can-i-see-the-sql-generated-by-sequelize-js/21431627#21431627) and just add:
```
logging: console.log,
```
to the code in the query you want to log.

## ↑ Ancestors (4)

1. [Log database queries](log-database-queries.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
