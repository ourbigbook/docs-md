# OurBigBook Web performance log

↑ **Parent:** [OurBigBook Web performance benchmarking](ourbigbook-web-performance-benchmarking.md)

A good benchmark for the critical Article page is perhaps the [Wikipedia bot](wikipedia-bot.md) account which stresses the atricle tree the hardest.

We should look out for metrics such as:
- First Contentful Paint (FCP)
- Time to First Byte (TTFB)
and test both on [Heroku deployment](heroku-deployment.md) and locally.

Local tests are always on optimized PostgresQL. Remote tests always on powerful home wifi, never 4G. Measuremnts are taken on browser Network tab in developer tools with cache enabled. Each URL is ran randomly a few times, which gives an idea of cache warmup effects. Logged-in is logged-in as `cirosantilli`.

Visit article:
- ae4d0e3a0964f3c00a7e1ec0d561ebd6f2d2f44f (show tagged headers under non-toplevel headers) TTFB logged off local:
  - /barack-obama: 60 - 75
  - /cirosantilli: 200 - 300
  - /wikibot: 100 - 120
- 3c61db4b778f0cc6c0fcfbc5519ef82927d365b3 (one before "show tagged headers under non-toplevel headers") TTFB logged off local:
  - /cirosantilli: 200 - 300
  - /wikibot: 110 - 120
- 075872a0a5ca7faf171d45834bc2b47995a15634 web: speed up article page DB queries further by moving topicId into topic

  At this commit we had highly optimized article page queries. The slowest query was getting the new upvotes of the logged in user at 20 - 30 ms.


  - TTFB
    - local
      - logged off:
        - /barack-obama: 40 - 60
        - /cirosantilli: 160 - 190
        - /cirosantilli/mathematics: 100 - 120
        - /wikibot: 65 - 70
      - logged in:
        - /barack-obama 65
        - /cirosantilli: 200 - 300
        - /wikibot: 90 - 100
    - cirosantilli.com: 100 - 200
    - ourbigbook.com
      - logged off:
        - /barack-obama: 140 -180
        - /cirosantilli: 300 - 400
        - /cirosantilli/mathematics: 240 - 400
        - /wikibot: 180 - 300
      - logged in:
        - /barack-obama: 250 - 400
        - /cirosantilli: 450 - 600
        - /cirosantilli/mathematics: 350 - 500
        - /wikibot: 330 - 450
- 8ea5ffa52d291350e9a5ddef92e4171d50a51dcc TTFB logged off:
  - local
    - /barack-obama: 400
    - /cirosantilli: 500
    - /wikibot: 1200
  - cirosantilli.com: 100 - 200
  - ourbigbook.com
    - /barack-obama: 500 - 700
    - /cirosantilli: 1100 - 1500
    - /wikibot: 3500 - 4500

  This suggests a database scaling issue like a missing index.

Update article:
- f2d48c4b6eaa6264017d3ef506a58167802730f3 Lenovo ThinkPad P14s Ubuntu 24.10 postgresql 16.8 and cirosantilli.github.io at 858d7eb936b541979660e3aecb7abf96541fc06c
  - /cirosantilli 380 ms
  - /cirosantilli/x86-paging and descendants 1900 ms
  - /cirosantilli/cool-data-embedded-in-the-bitcoin-blockchain and descendants 4400
  - /cirosantilli/cia-2010-covert-communication-websites and descendants 4700

Related:
- [Reach the same performance as static website with dynamic tree](todo/reach-the-same-performance-as-static-website-with-dynamic-tree.md)

## ↑ Ancestors (4)

1. [OurBigBook Web performance benchmarking](ourbigbook-web-performance-benchmarking.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Ourbigbook.com/cirosantilli loads 2x as fast after database optimizations](news/ourbigbook-com-cirosantilli-loads-2x-as-fast-after-database-optimizations.md)
