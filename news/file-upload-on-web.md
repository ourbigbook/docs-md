# File upload on Web

↑ **Parent:** [News](../news-split.md)

<a id="_9"></a>
It is now possible to have create file uploads on [OurBigBook Web](../ourbigbook-web.md), e.g.:<a id="_10"></a>

<a id="_11"></a>
- [https://ourbigbook.com/cirosantilli/_dir](https://ourbigbook.com/cirosantilli/_dir)
<a id="_12"></a>
- [https://ourbigbook.com/cirosantilli/_dir/c](https://ourbigbook.com/cirosantilli/_dir/c)
<a id="_13"></a>
- [https://ourbigbook.com/cirosantilli/_raw/c/segfault.c](https://ourbigbook.com/cirosantilli/_raw/c/segfault.c)
You can upload images, source code, or any other type of file.

<a id="_14"></a>
Previously, you'd just get broken links when publishing to [OurBigBook Web](../ourbigbook-web.md) if you linked to your files with the [`\a` macro](../link.md) or other related constructs.

<a id="_15"></a>
The implementation attempts to follow what already existed for [static websites](../p-publish.md) as closely as possible.

<a id="_16"></a>
The current implementation has a few limitations which should be fixed one day:<a id="_17"></a>

<a id="_18"></a>
- there is no web UI for file upload, it is exposed via CLI only
<a id="_19"></a>
- file previews don't show under corresponding `_file` articles as they do on static
<a id="_20"></a>
- `_file` articles are not properly auto-generated for files that don's have explicit articles, we just show `_raw` under `_file`

<a id="image-user-home-pages-have-a-link-to-the-root-file-directory-of-the-user"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/web-files/user-page-arrow.png" alt="" height="536">

**[Figure 1](#image-user-home-pages-have-a-link-to-the-root-file-directory-of-the-user). User home pages have a link to the root file directory of the user**. [Source](https://ourbigbook.com/cirosantilli).

<a id="image-sample-directory-listing"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/web-files/directory-listing.png" alt="" height="533">

**[Figure 2](#image-sample-directory-listing). Sample directory listing**. [Source](https://ourbigbook.com/cirosantilli/\_dir/c).

<a id="image-sample-raw-listing"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/web-files/raw.png" alt="" height="153">

**[Figure 3](#image-sample-raw-listing). Sample raw listing**. [Source](https://ourbigbook.com/cirosantilli/\_file/c/segfault.c).

<a id="_21"></a>
Announced at:<a id="_22"></a>

<a id="_23"></a>
- [https://mastodon.social/@ourbigbook/114851233133955275](https://mastodon.social/@ourbigbook/114851233133955275)
<a id="_24"></a>
- [https://x.com/OurBigBook/status/1944713518474744230](https://x.com/OurBigBook/status/1944713518474744230)
<a id="_25"></a>
- [https://www.linkedin.com/feed/update/urn:li:ugcPost:7350479547579961347](https://www.linkedin.com/feed/update/urn:li:ugcPost:7350479547579961347)
<a id="_26"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid02AH8MfRBf4Dc3LzoeGPnZkKp9GffS8qr2hF4FoqC9g1eq1EcGHV1ABcFiPniF4pual](https://www.facebook.com/OurBigBook/posts/pfbid02AH8MfRBf4Dc3LzoeGPnZkKp9GffS8qr2hF4FoqC9g1eq1EcGHV1ABcFiPniF4pual)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
