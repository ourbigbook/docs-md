<h1 id="ourbigbook-com-cirosantilli-loads-2x-as-fast-after-database-optimizations">ourbigbook.com/cirosantilli loads 2x as fast after database optimizations</h1>

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [OurBigBook Web performance benchmarking](../ourbigbook-web-performance-benchmarking.md), [`-W`, `--web`](../web.md)

At [https://github.com/ourbigbook/ourbigbook/commit/075872a0a5ca7faf171d45834bc2b47995a15634](https://github.com/ourbigbook/ourbigbook/commit/075872a0a5ca7faf171d45834bc2b47995a15634) and nearby previous commits we've optimized the database queries made on article pages, mostly by adding some key missing indices and cache columns.

As a result, [https://ourbigbook.com/cirosantilli](https://ourbigbook.com/cirosantilli) now starts downloading the first byte 2x as fast as before, going down from about 1200 ms to around 600 ms, at a time region which makes a huge difference for user experience.

We will also start keeping better performance logs at: [Section "OurBigBook Web performance log"](../ourbigbook-web-performance-log.md) to make sure we don't regress as easily.

Announcements:
- [https://mastodon.social/@ourbigbook/113068626468247721](https://mastodon.social/@ourbigbook/113068626468247721)
- [https://x.com/OurBigBook/status/1830626456235299211](https://x.com/OurBigBook/status/1830626456235299211)
- [https://www.linkedin.com/feed/update/urn:li:share:7236392360090243075](https://www.linkedin.com/feed/update/urn:li:share:7236392360090243075)
- [https://www.facebook.com/OurBigBook/posts/pfbid029F6xK7QrV725cAfFoVbb2RhGtKXvfzqBDcy2kvY1AALNSHDbnbuvZJkYFhzmejUcl](https://www.facebook.com/OurBigBook/posts/pfbid029F6xK7QrV725cAfFoVbb2RhGtKXvfzqBDcy2kvY1AALNSHDbnbuvZJkYFhzmejUcl)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
