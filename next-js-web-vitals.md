<h1 id="next-js-web-vitals">Next.js web vitals</h1>

↑ **Parent:** [OurBigBook Web performance benchmarking](ourbigbook-web-performance-benchmarking.md)

These are documented at [https://nextjs.org/docs/advanced-features/measuring-performance](https://nextjs.org/docs/advanced-features/measuring-performance). To enable them use `NEXT_PUBLIC_OURBIGBOOK_LOG_PERF`, the front-end-avaible version of [`OURBIGBOOK_LOG_PERF`](ourbigbook-log-perf.md):
```
NEXT_PUBLIC_OURBIGBOOK_LOG_PERF=1 npm run dev
```

If enabled, we see a few metrics printed on the browser console such as:
```
{
    "id": "1667591558646-5510113745482",
    "name": "TTFB",
    "startTime": 0,
    "value": 2474.199999999255,
    "label": "web-vital"
}
{
    "id": "1667591558646-9119282792899",
    "name": "LCP",
    "startTime": 4982.099,
    "value": 4982.099,
    "label": "web-vital"
}
```

## ↑ Ancestors (4)

1. [OurBigBook Web performance benchmarking](ourbigbook-web-performance-benchmarking.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
