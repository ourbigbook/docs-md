<h1 id="force-render">-<code>F</code>, <code>--force-render</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Always render all selected files, irrespectively of if they are known to be outdated or not.

OurBigBook stores the timestamp of the last successful [ID extraction](id-extraction.md) step for each file.

For [ID extraction](id-extraction.md), we always skip the extraction if the filesystem timestamp of a source file is older than the last successful extraction.

For render:
- we mark output files as outdated when the corresponding source file is parsed
- we also skip rendering non-outdated files by default when you invoke ourbigbook on a directory, e.g. `ourbigbook .`, as this greatly speeds up the interactive error fixing turnaround time
- we always re-render fully when you specify a single file, e.g. `ourbigbook path/to/index.bigb`

However, note that skipping renders, unlike for ID extraction, can lead to some outdated pages.

This option disables the timestamp skip for rendering, so ensure that you will get a fully clean updated render.

E.g. consider if you had two files:

file1.bigb

```
= File 1

== File 1 1
```

file2.bigb

```
= File 2

== File 2 1

\x[file-1-1]
```

We then do the initial conversion:
```
ourbigbook .
```
we see output like:
```
extract_ids file1.bigb
extract_ids file1.bigb finished in 45.61287499964237 ms
extract_ids file2.bigb
extract_ids file2.bigb finished in 15.163879998028278 ms
render file1.bigb
render file1.bigb finished in 23.21016100049019 ms
render file2.bigb
render file2.bigb finished in 25.92908499762416 ms
```
indicating full conversion without skips.

But then if we just modify fil1.bigb as:
```
= File 1

== File 1 1 hacked
{id=file-1-1}
```
the following conversion with `ourbigbook .` would look like:
```
extract_ids file1.bigb
extract_ids file1.bigb finished in 45.61287499964237 ms
extract_ids file2.bigb
extract_ids file2.bigb skipped by timestamp
render file1.bigb
render file1.bigb finished in 41.026930000633 ms
render file2.bigb
render file2.bigb skipped by timestamp
```
and because we skipped `file2.bigb` render, it will still have the outdated "File 1 1" instead of "File 1 1 hacked".

We could in principle solve this problem by figuring out exactly which files need to be changed when a given ID changes, and we already [have to solve a similar problem due to query bundling](conversion-process-overview.md). Also, this will need to be done sonner or later for the [OurBigBook Web](ourbigbook-web.md). But lazy now: [https://github.com/ourbigbook/ourbigbook/issues/207](https://github.com/ourbigbook/ourbigbook/issues/207), this is hard stuff.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`--web-force-render`](web-force-render.md)
