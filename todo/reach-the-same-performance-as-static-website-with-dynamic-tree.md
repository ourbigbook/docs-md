# Reach the same performance as static website with dynamic tree

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Performance](performance.md), [Web](web.md)

The move to dynamic tree slowed things down a lot for large pages such as: [https://ourbigbook.com/cirosantilli](https://ourbigbook.com/cirosantilli), making it is just unacceptably slow, and actually blocks any other page loads as the server does work.

These were at cirosantilli.github.io at aa60ccb934bf9646d548e6b761489d31aec1a341, which has almost 7k articles.

Some benchmarks on Chromium:
- `ping cirosantilli.com`: 17 ms
- [https://cirosantilli.com](https://cirosantilli.com) `GET /`: 1.3s. Waiting for server: ping time only, the rest is content download. `content-length` from response: 300 kB zipped.
- [https://ourbigbook/cirosantilli](https://ourbigbook/cirosantilli) `GET /`:
  - Waiting for server response: 3.5s to 4s. That's our problem!
  - Contend download: 2.5s
- [http://localhost:3000/cirosantilli](http://localhost:3000/cirosantilli) `npm run dev` `GET /`:
  - Waiting for server response: between 2 and 3s. So we reproduce relatively well locally.

    curl `time_starttransfer` after a few stabilizing runs: 2.6s
  - Contend download: 1.6s

If we comment the single line in Article.tsx:
```
//html += renderTocFromEntryList({ entry_list })
```
TTFB falls from 2.6s to 0.77s.

Removing the `renderRefCallback` drops it to between 2.2 and 2.4.

Limiting the ToC to 1k articles on server side leads to 0.5s. Maybe that's the first workaround we have to do until something else is understood. It is a shame that we have to go so much lower than the static website.

Maybe we can use some of the techniques from: [https://reactjs.org/docs/optimizing-performance.html#virtualize-long-lists](https://reactjs.org/docs/optimizing-performance.html#virtualize-long-lists) to improve things.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (2)

- [OurBigBook Web performance log](../ourbigbook-web-performance-log.md)
- [Inject React header metadata on each header separately](inject-react-header-metadata-on-each-header-separately.md)
