# Speed comparison to other markup language implementations

↑ **Parent:** [Performance](performance.md)

One quick and dirty option is to use `generate-paragraphs` which generates output compatible for most markup languages:
```
./generate-paragraphs 100000 > tmp.bigb
```

On Ubuntu 20.04 [Lenovo ThinkPad P51](https://cirosantilli.com/linux-kernel-module-cheat/#p51) for example:
- OurBigBook 54ba49736323264a5c66aa5d419f8232b4ecf8d0 + 1, Node.js v12.18.1
  ```
  time ./ourbigbook tmp.bigb
  ```

  outputs:
  ```
  real    0m5.104s
  user    0m6.323s
  sys     0m0.674s
  ```
- Asciidoctor 2.0.10, Ruby 2.6.0p0:
  ```
  cp tmp.bigb tmp.adoc
  time asciidoctor tmp.adoc
  ```

  outputs:
  ```
  real    0m1.911s
  user    0m1.850s
  sys     0m0.060s
  ```
- [cmark](https://github.com/commonmark/cmark) 0.29.0:
  ```
  cp tmp.bigb tmp.md
  time cmark tmp.md > tmp.md.html
  ```

  outputs:
  ```
  real    0m0.091s
  user    0m0.070s
  sys     0m0.021s
  ```

  Holy cow, it is 200x faster than Asciidoctor!
- [markdown-it](https://github.com/markdown-it/markdown-it) at 5789a3fe9693aa3ef6aa882b0f57e0ea61efafc0 to get an idea of a JavaScript markdown implementation:
  ```
  time markdown-it tmp.md > tmp.md.html
  ```

  outputs:
  ```
  real    0m0.361s
  user    0m0.590s
  sys     0m0.060s
  ```
- `cat` just to find the absolute floor:
  ```
  time cat tmp.bigb > tmp.tmp
  ```

  outputs:
  ```
  real    0m0.006s
  user    0m0.006s
  sys     0m0.000s
  ```

## ↑ Ancestors (3)

1. [Performance](performance.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)
