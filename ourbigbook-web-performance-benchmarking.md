# OurBigBook Web performance benchmarking

↑ **Parent:** [OurBigBook Web development](ourbigbook-web-development.md)

[https://stackoverflow.com/questions/18215389/how-do-i-measure-request-and-response-times-at-once-using-curl](https://stackoverflow.com/questions/18215389/how-do-i-measure-request-and-response-times-at-once-using-curl) is a useful one if the server is slow:
```
curl -o /dev/null -s -w 'Establish Connection: %{time_connect}s\nTTFB: %{time_starttransfer}s\nTotal: %{time_total}s\n' http://localhost:3000
```

**Table of contents**

- [Next.js web vitals](next-js-web-vitals.md)
- [`OURBIGBOOK_LOG_PERF`](ourbigbook-log-perf.md)
- [OurBigBook Web performance log](ourbigbook-web-performance-log.md)

## 🏷️ Tagged (1)

- [Ourbigbook.com/cirosantilli loads 2x as fast after database optimizations](news/ourbigbook-com-cirosantilli-loads-2x-as-fast-after-database-optimizations.md)

## ↑ Ancestors (3)

1. [OurBigBook Web development](ourbigbook-web-development.md)
2. [OurBigBook Web](ourbigbook-web.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`--web-max-renders`](web-max-renders.md)
