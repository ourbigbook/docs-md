# Demo data local file output

↑ **Parent:** [Demo data](demo-data.md)

By default, when you run [web/bin/generate-demo-data.js](web/bin/generate-demo-data.js), besides inserting the data into the database directly, the command also generates a in-file-system tree that contains equivalent content under:
```
web/tmp/<username>/<id>.bigb
```

Sample paths to some files could be:
```
web/tmp/demo/barack-obama/ourbigbook.json
web/tmp/demo/barack-obama/test-child-1.bigb
web/tmp/demo/barack-obama/test-scope/test-scope-1.bigb
```

Because each user has its own `ourbigbook.json` file added to the directory, you can for example build each user directory in isolation with:
```
cd web/tmp/demo/barack-obama
ourbigbook .
```

This setup can be useful for quickly testing things locally, and in particular to test [`-W`, `--web`](web.md) upload to a local test server.

These files have nothing to do with [OurBigBook Web](ourbigbook-web.md) specifically, and would be used from [OurBigBook CLI](ourbigbook-cli.md) itself. It would be nice to bring them up to [OurBigBook CLI](ourbigbook-cli.md) at some point, and only expose the Web-specific database functions from Web.

## ↑ Ancestors (5)

1. [Demo data](demo-data.md)
2. [Generated data](generated-data.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
