<h1 id="ourbigbook-log-db"><code>OURBIGBOOK_LOG_DB</code></h1>

↑ **Parent:** [Log database queries](log-database-queries.md)  
🏷️ **Tags:** [OurBigBook Web environment variable](ourbigbook-web-environment-variable.md)

This tends to be a better good way for benchmarking than [DEBUG sql](debug-sql.md):
```
OURBIGBOOK_LOG_DB=1 npm run dev
```
which sets in the Sequelize constructor:
```
rew Sequelize({ logging: console.log })
```
and produces many outputs of type:
```
Executed (default): SELECT 1+1 AS result Elapsed time: 0ms
```
so we get explicit elapsed time measurements rather than deltas, and without the corresponding `Executing` marker.

Furthermore, because we try to code the server correctly by making multiple `async` requests simultaneously wherever possible, the slowest of those requests finishes, last, and is the last "Elapsed time" to get logged! So you generally just have to look at the last logged line if there's one slow bottleneck query, rather than going over all the previous "Elapsed time" entries.

This method uses Sequelize's `benchamrk: true` option as per: [https://stackoverflow.com/questions/52260934/how-to-measure-query-execution-time-in-seqilize](https://stackoverflow.com/questions/52260934/how-to-measure-query-execution-time-in-seqilize).

## ↑ Ancestors (4)

1. [Log database queries](log-database-queries.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
