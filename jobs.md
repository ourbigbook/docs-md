<h1 id="jobs"><code>-j</code>, <code>--jobs &lt;n&gt;</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Directory builds use the available CPUs by default:
```
ourbigbook .
```

Use `-j N` or `--jobs N` to limit the number of worker processes. For example, `ourbigbook -j 4 .` uses up to four workers, and `ourbigbook -j 1 .` builds serially. The default is the number of CPUs available to the process, respecting CPU affinity. Workers are started only for files that need conversion and reused throughout the build.

There are two parallel conversion stages, separated by a database check:
- extract IDs from source files in parallel
- wait for all extraction to finish, then run the [database consistency check](check-db-only.md) once, serially
- render in parallel using the checked IDs and references

Extraction or database errors stop the build before rendering. [`--no-render`](no-render.md) runs only extraction and the database check. Timestamp-based skipping still applies in both stages.

SQLite uses write-ahead logging so readers can run while a writer commits. Only one worker at a time may update the ID database; the whole per-file transaction holds that write lock. Workers use fresh reference caches for each conversion. Generated file previews also render in parallel, before authored pages so explicit file headers retain precedence. Asset copying, Sass compilation, and directory listings remain serial.

Web builds also extract IDs and render local split files in parallel, using the same `-j` setting. Updates to the local Web article cache are serialized. Uploads and server-side `web_render` requests remain serial.

Single-file conversions, watch mode, source formatting, embedded includes, and builds without a persistent database retain their serial behavior.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
