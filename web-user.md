<h1 id="web-user"><code>--web-user</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Set the username for [`-W`, `--web`](web.md) from the command line, e.g.:
```
ourbigbook --web --web-url http://localhost:3000 --web-user barack-obama
```
If not given:
- use the latest previous successfull web login with `ourbigbook --web` if there are any. In that case, the CLI informs you with a message of type:
  ```
  Using previous username: barack-obama
  ```
- otherwise, you will be prompted for it from the command line.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
