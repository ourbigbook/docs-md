# Short URL fragments on OurBigBook Web

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [Dynamic article tree](../ourbigbook-web-dynamic-article-tree.md), [Implemented by sidstuff](../implemented-by-sidstuff.md), [OurBigBook Web](../ourbigbook-web.md)

<a id="_351"></a>
Previously, when clicking a link to an element that is present in the current page, the URL fragment would contain the full ID that element.

<a id="_352"></a>
Now, only the ID relative to URL path shows.

<a id="_353"></a>
A very common use case for this is when clicking table of content items.

<a id="_354"></a>
For exmple, from [https://ourbigbook.com/barack-obama/mathematics](https://ourbigbook.com/barack-obama/mathematics), clicking the ToC item for "Calculus" would previously lead to [https://ourbigbook.com/barack-obama/mathematics#barack-obama/calculus](https://ourbigbook.com/barack-obama/mathematics#barack-obama/calculus)

<a id="_355"></a>
After this change it leads just to: [https://ourbigbook.com/barack-obama/mathematics#calculus](https://ourbigbook.com/barack-obama/mathematics#calculus), without repeating the "`#barack-obama` part as it already appears in the URL path `/barack-obama/mathematics`.

<a id="_356"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/short-fragment.png" alt="" height="800">

<a id="_357"></a>
Short URLs were already used on [Static website](../p-publish.md) publishes, and weren't implemented on [OurBigBook Web](../ourbigbook-web.md) yet simply because this is hard. The reason this was much harder to implement on Web is that due to [Dynamic article trees](../ourbigbook-web-dynamic-article-tree.md) we can't know at render-time what the correct fragment will be, as it depends on what shows on the page or not.

<a id="_358"></a>
And furthermore, articles by different users can appear on the same page due to [topics](../ourbigbook-web-topics.md).

<a id="_359"></a>
The simple but not ideal solution that we were using up to now was to just have full IDs on every HTML element, make every a point to an absolute ID like `/barack-obama/mathematics`, and then use JS effect to hack that to `#barack-obama/mathematics` if the element is in the page.

<a id="_360"></a>
What we did now is to take the Js hacks one step further, and actually replace the "long URLs" with short ones. This was not easy, partly because the browser interfaces are not amazing in that area, partly due to fighting with React. But we manage to get it working mostly well.

<a id="_361"></a>
Announcements:<a id="_362"></a>

<a id="_363"></a>
- [https://mastodon.social/@ourbigbook/112553597134131989](https://mastodon.social/@ourbigbook/112553597134131989)
<a id="_364"></a>
- [https://x.com/OurBigBook/status/1797665231273177182](https://x.com/OurBigBook/status/1797665231273177182)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
