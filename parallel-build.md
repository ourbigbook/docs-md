# Parallel build

↑ **Parent:** [OurBigBook CLI](ourbigbook-cli.md)

TODO: get this working. Maybe we should also bake it into the `ourbigbook` CLI tool as well for greater portability. Starting like this as a faster way to prototype:
```
rm -rf _out/parallel
mkdir -p _out/parallel
# ID extraction.
git ls-files | grep -E '\.bigb$' | parallel -X ourbigbook --no-render --no-check-db --outdir '_out/parallel/{%}' '{}'
./merge-dbs _out/db.sqlite3 _out/parallel/*/db.sqlite3
ourbigbook --check-db
# Render.
git ls-files | grep -E '\.bigb$' | parallel -X ourbigbook --no-check-db '{}'
```

Observed `--no-render`  speedup on 1k small files from the [Wikipedia bot](wikipedia-bot.md) and 8 cores: 3x. So not bad.

Observed render speedup on 1k small files from the [Wikipedia bot](wikipedia-bot.md) and 8 cores: none. TODO. Is this because of database contention?

## ↑ Ancestors (2)

1. [OurBigBook CLI](ourbigbook-cli.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`--check-db-only`](check-db-only.md)
- [`--no-check-db`](no-check-db.md)
