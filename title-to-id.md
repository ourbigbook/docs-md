<h1 id="title-to-id"><code>--title-to-id</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Read tiles from stdin line by line on a while loop and output IDs to stdout only, performing [automatic ID from title](automatic-id-from-title.md) conversion on each input line.

Sample usage:
```
( echo 'Hello world'; sleep 1; echo 'C++ is great'; sleep 1; echo 'β Centauri' ) | ourbigbook --title-to-id
```
outputs:
```
hello-world
c-plus-plus-is-great
beta-centauri
```
each with one second intervals between each line.

The original application of this option was to allow external non Node.js processes to be able to accurately calculate IDs from human readable titles since the non-ASCII handling of the algorithm is complex, and hard to reimplement accurately.

From Python for example one may run something like:

```
from subprocess import Popen, PIPE, STDOUT
import time

p = Popen(['ourbigbook', '--title-to-id'], stdout=PIPE, stdin=PIPE)

p.stdin.write('Hello world\n'.encode())
p.stdin.flush()
print(p.stdout.readline().decode()[:-1])

time.sleep(1)

p.stdin.write('bonne journeé\n'.encode())
p.stdin.flush()
print(p.stdout.readline().decode()[:-1])
```

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
