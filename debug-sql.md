# DEBUG sql

↑ **Parent:** [Log database queries](log-database-queries.md)

One option is to use the standard Express.js logging mechanism:
```
DEBUG='sequelize:sql:*' npm run dev
```
Shortcut:
```
npm run devs
```

These logs also include some kind of timing information. However, we are not entirely sure that the timings mean, as they show for both `Executing` (query is about to start) and `Executed` (query finished) lines with possibly different values e.g.:
```
sequelize:sql:pg Executing (default): SELECT 1+1 AS result +0ms
sequelize:sql:pg Executed (default): SELECT 1+1 AS result +1ms
```
The meaning of `+0ms` and `+1ms` appears to be the timing since last the last message with the same ID, i.e. `sequelize:sql:pg` in this case. Therefore, so long as there wasn't any `sequelize:sql:pg` between and the corresponding `Executing`, the `Executing` timing should give us the query time.

This is a bit messy however, as we often want to find the largest numbers for profiling, and there could be a large time delta during inactivity.

## ↑ Ancestors (4)

1. [Log database queries](log-database-queries.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`OURBIGBOOK_LOG_DB`](ourbigbook-log-db.md)
