# Optimize generated HTML size by adding on-the-fly elements

↑ **Parent:** [News](../news-split.md)

<a id="_430"></a>
The main focus was the [Table of contents](../table-of-contents.md) rendering, which had a lot of redundant stuff. Headers were the next largest gain.

<a id="_431"></a>
The main techniques used to reduce size were:<a id="_432"></a>

<a id="_433"></a>
- auto-generate a few elements on-the-fly with JavaScript for on-hover effects, but only if it doesn't affect SEO and readability when JS is turned off
<a id="_434"></a>
- use a lot more CSS `::after` and `::before` to avoid embedding repetitive icons multiple times on the HTML

<a id="_435"></a>
After this changes, the rendered size of cirosantilli.com fell from 216 MiB to 156.5 MiB, which is kind of cool!

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
