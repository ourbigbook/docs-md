# Cross file internal link internals

↑ **Parent:** [Cross file internal link](cross-file-internal-link.md)

When running in Node.js, OurBigBook dumps the IDs of all processed files to a `_out/db.sqlite3` file in [the `_out` directory](the-out-directory.md), and then reads from that file when IDs are needed.

When converting under a directory that contains [`ourbigbook.json`](ourbigbook-json.md), `_out/db.sqlite3` is placed inside the same directory as the `ourbigbook.json` file.

If there is no `ourbigbook.json` in parent directories, then `_out/db.sqlite3` is placed in the current working directory.

These follows the principles described at: [the current working directory does not matter when there is a `ourbigbook.json`](the-current-working-directory-does-not-matter-when-there-is-a-ourbigbook-json.md).

`db.sqlite3` is not created or used when handling input from [stdin](stdin-conversion.md).

When running in the browser, the same JavaScript API will send queries to the server instead of a local SQLite database.

To inspect the ID database to debug it, you can use:
```
sqlite3 _out/db.sqlite3 .dump
```

It is often useful to dump a single table, e.g. to dump the `ids` table:
```
sqlite3 _out/db.sqlite3 '.dump ids'
```
and one particularly important query is to dump a list of all known IDs:
```
sqlite3 _out/db.sqlite3 'select id from ids'
```

You can force `ourbigbook` to not use the ID database with the [`--no-db`](no-db.md) command line option

## ↑ Ancestors (5)

1. [Cross file internal link](cross-file-internal-link.md)
2. [Internal link](internal-link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Include](include.md)
- [OurBigBook Library](ourbigbook-library.md)
- [The `_out` directory](the-out-directory.md)
