<h1 id="web-bin-benchmark"><code>web/bin/benchmark</code></h1>

↑ **Parent:** [OurBigBook Web performance benchmarking](ourbigbook-web-performance-benchmarking.md)

With the web server running at `http://localhost:3000`, run from the repository root:
```
web/bin/benchmark
```

This appends a run to `../ourbigbook-media/benchmark.json`, creating its directory if needed. The file is a JSON array with the oldest run first. Repeated runs of the same commit are kept separately. Each entry contains:
- `about`: UTC start and finish timestamps, Git SHA and dirty status, database object counts, PostgreSQL version and settings, OS distribution and version when available (e.g. Ubuntu version), hostname, CPU, memory, Node.js version, and benchmark options.
- `results`: request paths mapped to median elapsed milliseconds.
- `samples`: individual measured timings in milliseconds.
- `errors`: failed requests; their `results` value is `null`.

Requests run sequentially and anonymously, with one warmup and three measured requests per path. Timings include reading the entire response body. The selected calls cover articles, topics, users, discussions, comments, upload hashes, author/follow queries, search, and sorting variants. List APIs are sampled at their first, middle, and last pages. The author with the most articles is selected by default. Relevant HTML listing pages are also measured because they apply different filters and sorting rules from the API, including the global article list.

Use `--api-only` to skip HTML pages, `--author USERNAME` to select an author, `--runs N` and `--warmup N` to change sampling, `--timeout MS` to change the default 60-second request timeout, or `--output PATH` to change the history file. Progress is saved after each path. An error stops the run, saves partial results, and returns a nonzero exit status.

To capture PostgreSQL execution plans as well, start the server with:
```
OURBIGBOOK_EXPLAIN=1 npm run dev-pg --prefix web
```
Then benchmark it with:
```
web/bin/benchmark
```

This uses [PostgreSQL auto\_explain](https://www.postgresql.org/docs/current/auto-explain.html) to instrument the original SQL execution, including writes, without executing queries a second time. PostgreSQL must have the module installed and the database role must have superuser permission to load and configure it. Actual row counts and buffer statistics are collected; per-node timing is disabled to reduce overhead. Session/transaction commands without execution plans still appear in the trace with an empty `plans` array. Failed queries include their error.

For the default local database role, grant the required permission with:
```
sudo -u postgres psql -c 'ALTER ROLE ourbigbook_user SUPERUSER;'
```
If `DATABASE_URL` uses another role, substitute its username. Restart the web server after changing the role. To remove the privilege after profiling, run:
```
sudo -u postgres psql -c 'ALTER ROLE ourbigbook_user NOSUPERUSER;'
```

Query-plan collection is enabled by default: the benchmark detects tracing from the server's response headers. If tracing is disabled on the server, it continues normally without creating a plans file. Use `--no-explain` to disable collection explicitly.

The server temporarily saves request traces under `tmp/benchmark-explain`. The benchmark moves them into `benchmark/RUN_ID.explain.jsonl` relative to the results file. With the default output, plans are therefore stored under `../ourbigbook-media/benchmark`. Each JSONL line contains one HTTP request's SQL, bind parameters, plans, request ID, and warmup/sample iteration. The run's `explain.file` and `explain.requests` link timings to those records. `about.db_instrumentation` marks instrumented runs: their timings include instrumentation overhead and should be compared with other instrumented runs.

Server and benchmark must share the trace directory. To use another directory, set `OURBIGBOOK_EXPLAIN=/absolute/path` on the server and pass `--explain /absolute/path` to the benchmark. The benchmark also reads `OURBIGBOOK_EXPLAIN` when set in its own environment. Traces contain SQL and parameter values and are written as private local files, rather than exposed through an HTTP endpoint. Disable the server variable when finished profiling.

The benchmark detects PostgreSQL or SQLite from the running server's `/api/` response before loading database configuration. No `--sqlite` option is needed. For PostgreSQL, set the same connection environment variables (`DATABASE_URL`, `OURBIGBOOK_DB_NAME`) as the server; for SQLite, metadata is read from `web/db.sqlite3`. This detection makes one preliminary request outside the measured timings. Rebuild or restart the server for the commit being measured: the recorded Git SHA identifies the local checkout. Use the same data and server mode when comparing runs.

## ↑ Ancestors (4)

1. [OurBigBook Web performance benchmarking](ourbigbook-web-performance-benchmarking.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
