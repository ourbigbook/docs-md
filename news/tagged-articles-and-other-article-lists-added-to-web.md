# Tagged articles and other article lists added to Web

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [`-W`, `--web`](../web.md)

<a id="_186"></a>
For some time we have been listing certain ["cross article" metadata](../header-metadata-section.md) at the bottom of articles on both [`-W`, `--web`](../web.md) and [static](../p-publish.md).

<a id="_187"></a>
For example, on both:<a id="_188"></a>

<a id="_189"></a>
- [https://cirosantilli.com/classification-mathematics](https://cirosantilli.com/classification-mathematics)
<a id="_190"></a>
- [https://ourbigbook.com/cirosantilli/classification-mathematics](https://ourbigbook.com/cirosantilli/classification-mathematics)
you can see a list of articles tagged by the given articles at the end of the page.

<a id="_191"></a>
Now, only on [`-W`, `--web`](../web.md), you can also see these article lists with the article content itself, for example:<a id="_192"></a>

<a id="_193"></a>
- <a id="_194"></a>
  tagged: [https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics)

  <a id="image-ourbigbook-web-tagged-article-list-with-body-demo"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/tagged.png" alt="" height="1081">

  **[Figure 19](#image-ourbigbook-web-tagged-article-list-with-body-demo). OurBigBook Web tagged article list with body demo**. Live URL: [https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics)

  <a id="_195"></a>
  Accessible via header links to the Tagged sections both on toplevel and non-toplevel:

  <a id="image-ourbigbook-web-toplevel-header-link-to-tagged-article-list"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/toplevel-to-tagged-arrow.png" alt="" height="736">

  **[Figure 20](#image-ourbigbook-web-toplevel-header-link-to-tagged-article-list). OurBigBook Web toplevel header link to tagged article list**. Live URL: [https://ourbigbook.com/cirosantilli/classification-mathematics](https://ourbigbook.com/cirosantilli/classification-mathematics)

  <a id="image-ourbigbook-web-non-toplevel-header-link-to-tagged-article-list"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/not-toplevel-to-tagged-arrow.png" alt="" height="783">

  **[Figure 21](#image-ourbigbook-web-non-toplevel-header-link-to-tagged-article-list). OurBigBook Web non-toplevel header link to tagged article list**. Live URL: [https://ourbigbook.com/cirosantilli/the-beauty-of-mathematics#classification-mathematics](https://ourbigbook.com/cirosantilli/the-beauty-of-mathematics#classification-mathematics)
<a id="_196"></a>
- <a id="_197"></a>
  incoming links: [https://ourbigbook.com/go/user/cirosantilli/incoming/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/incoming/classification-mathematics)

  <a id="image-ourbigbook-web-incoming-article-list-with-body-demo"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/incoming.png" alt="" height="1048">

  **[Figure 22](#image-ourbigbook-web-incoming-article-list-with-body-demo). OurBigBook Web incoming article list with body demo**. Live URL: [https://ourbigbook.com/go/user/cirosantilli/incoming/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/incoming/classification-mathematics)
<a id="_198"></a>
- <a id="_199"></a>
  children: [https://ourbigbook.com/go/user/cirosantilli/children/mammal-subclade](https://ourbigbook.com/go/user/cirosantilli/children/mammal-subclade)

  <a id="image-ourbigbook-web-incoming-child-list-with-body-demo"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/children.png" alt="" height="989">

  **[Figure 23](#image-ourbigbook-web-incoming-child-list-with-body-demo). OurBigBook Web incoming child list with body demo**. Live URL: [https://ourbigbook.com/go/user/cirosantilli/children/mammal-subclade](https://ourbigbook.com/go/user/cirosantilli/children/mammal-subclade)

  <a id="_200"></a>
  Accessible via the newly added "was limited to" info boxes when there are too many articles under a tree to show on the page:

  <a id="image-ourbigbook-web-limited-toc-size-link-to-full-child-article-list"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/limited-to-toc-arrow.png" alt="" height="620">

  **[Figure 24](#image-ourbigbook-web-limited-toc-size-link-to-full-child-article-list). OurBigBook Web limited ToC size link to full child article list**. Live URL: [https://ourbigbook.com/cirosantilli/mathematics](https://ourbigbook.com/cirosantilli/mathematics)

  <a id="image-ourbigbook-web-limited-descendant-articles-link-to-full-child-article-list"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/limited-to-articles-arrow.png" alt="" height="822">

  **[Figure 25](#image-ourbigbook-web-limited-descendant-articles-link-to-full-child-article-list). OurBigBook Web limited descendant articles link to full child article list**. Live URL: [https://ourbigbook.com/cirosantilli/mathematics](https://ourbigbook.com/cirosantilli/mathematics)

<a id="_201"></a>
The initial motivation for this was to be able to quickly browse through tagged articles, especially since the recent [tagged headers show under non-toplevel headers](tagged-headers-show-under-non-toplevel-headers.md).

<a id="_202"></a>
Another motivation for this is the ability to be able to view such lists with pagination when a large number of items exists. While we don't currently limit tagged and incoming links listings, children listings are already useful as we currently limit [dynamic article tree](../ourbigbook-web-dynamic-article-tree.md) ToCs to 1000 entries, so that children listings open up a way to explore such large article trees.

<a id="_203"></a>
This is the type of cute thing that can only be done efficiently on [`-W`, `--web`](../web.md), where we can use an actual database to build up a precise response as requested. On [static websites](../p-publish.md), this would either require lots of repetition on pre-rendered HTML, or making several JavaScript requests to fetch individual articles from the server, which could risk overloading the server.

<a id="_204"></a>
Announcements:<a id="_205"></a>

<a id="_206"></a>
- [https://mastodon.social/@ourbigbook/113641150832674015](https://mastodon.social/@ourbigbook/113641150832674015)
<a id="_207"></a>
- [https://x.com/OurBigBook/status/1867268408879845818](https://x.com/OurBigBook/status/1867268408879845818)
<a id="_208"></a>
- [https://www.linkedin.com/feed/update/urn:li:ugcPost:7273034333219655680/](https://www.linkedin.com/feed/update/urn:li:ugcPost:7273034333219655680/)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
