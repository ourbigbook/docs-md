<h1 id="log-perf"><code>--log perf</code></h1>

↑ **Parent:** [`--log`](log.md)

print [performance](performance.md) statistics to stderr, for example
```
./ourbigbook --log=perf index.bigb
```
could output:
```
perf start: 181.33060800284147
perf tokenize_pre: 181.4424349963665
perf tokenize_post: 318.333980999887
perf parse_start: 319.1866770014167
perf post_process_start: 353.5477180033922
perf post_process_end: 514.1527540013194
perf render_pre: 514.1708239987493
perf render_post: 562.834307000041
perf end: 564.0349840000272
perf convert_input_end 566.1234430000186
perf convert_path_pre_sqlite 566.1564619988203
perf convert_path_pre_sqlite_transaction 566.2528780028224
perf convert_path_post_sqlite_transaction 582.256645001471
perf convert_path_end 582.3469280004501
```
which shows how long different parts of the [conversion process](conversion-process-overview.md) took to help identify bottlenecks.

This option can also be useful to mark phases of the conversion to identify from which phase other logs are coming from, e.g. if we wanted to know which part of the conversion is making a ton of database requests we could run:
```
ourbigbook --log db perf -- index.bigb
```
and we would see the database requests made at each conversion phase.

Note that `--log perf` currently does not take sub-converts into account, e.g. [include](include.md) and [`\OurBigBookExample`](ourbigbookexample.md) both call the toplevel conversion  function `convert`, and therefore go through all the conversion intervals, but we do not take those it account, and just dump them all into the same toplevel interval that they happen in, currently between `post_process_start` and `post_process_end`.

## ↑ Ancestors (4)

1. [`--log`](log.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Conversion process overview](conversion-process-overview.md)
- [`--log`](log.md)
