# Reach the same performance as static website with dynamic tree

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Performance](performance.md), [Web](web.md)

<a id="_242"></a>
The move to dynamic tree slowed things down a lot for large pages such as: [https://ourbigbook.com/cirosantilli](https://ourbigbook.com/cirosantilli), making it is just unacceptably slow, and actually blocks any other page loads as the server does work.

<a id="_243"></a>
These were at cirosantilli.github.io at aa60ccb934bf9646d548e6b761489d31aec1a341, which has almost 7k articles.

<a id="_244"></a>
Some benchmarks on Chromium:<a id="_245"></a>

<a id="_246"></a>
- `ping cirosantilli.com`: 17 ms
<a id="_247"></a>
- [https://cirosantilli.com](https://cirosantilli.com) `GET /`: 1.3s. Waiting for server: ping time only, the rest is content download. `content-length` from response: 300 kB zipped.
<a id="_248"></a>
- [https://ourbigbook/cirosantilli](https://ourbigbook/cirosantilli) `GET /`:<a id="_249"></a>

  <a id="_250"></a>
  - Waiting for server response: 3.5s to 4s. That's our problem!
  <a id="_251"></a>
  - Contend download: 2.5s
<a id="_252"></a>
- [http://localhost:3000/cirosantilli](http://localhost:3000/cirosantilli) `npm run dev` `GET /`:<a id="_253"></a>

  <a id="_254"></a>
  - <a id="_255"></a>
    Waiting for server response: between 2 and 3s. So we reproduce relatively well locally.

    <a id="_256"></a>
    curl `time_starttransfer` after a few stabilizing runs: 2.6s
  <a id="_257"></a>
  - Contend download: 1.6s

<a id="_258"></a>
If we comment the single line in Article.tsx:<a id="_259"></a>

```
//html += renderTocFromEntryList({ entry_list })
```
TTFB falls from 2.6s to 0.77s.

<a id="_260"></a>
Removing the `renderRefCallback` drops it to between 2.2 and 2.4.

<a id="_261"></a>
Limiting the ToC to 1k articles on server side leads to 0.5s. Maybe that's the first workaround we have to do until something else is understood. It is a shame that we have to go so much lower than the static website.

<a id="_262"></a>
Maybe we can use some of the techniques from: [https://reactjs.org/docs/optimizing-performance.html#virtualize-long-lists](https://reactjs.org/docs/optimizing-performance.html#virtualize-long-lists) to improve things.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (2)

- [OurBigBook Web performance log](../ourbigbook-web-performance-log.md)
- [Inject React header metadata on each header separately](inject-react-header-metadata-on-each-header-separately.md)
