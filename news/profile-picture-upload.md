# Profile picture upload

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [`-W`, `--web`](../web.md)

<a id="_165"></a>
You can now update your profile picture on [OurBigBook Web](../ourbigbook-web.md) by uploading an image to the website like in a normal website.

<a id="_166"></a>
Previously, we only supported linking to an external image URL. Now this is not allowed anymore and you must instead upload your image to the website. Existing external links will continue to work, but if you want to update the profile picture again, then you will need to upload your own next time.

<a id="_167"></a>
Besides being a basic feature expected from any modern website, this is the first instance of "static file upload" on the site, and serves as part of a more general static file upload mechanism that can be later reused for other important features like uploading images for your articles.

<a id="_168"></a>
This initial implementation is very simplistic: we are just storing the image directly in the database. We will look into migrating to a more proper static file solution later on if this starts to hurt performance. We're using the [sharp](https://github.com/lovell/sharp) Node.js image processing library, a frontend to [libvips](https://github.com/libvips/libvips), to downsize input images as needed.

<a id="image-ourbigbook-web-profile-picture-upload"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/profile-picture/update-arrow.png" alt="" height="800">

**[Figure 17](#image-ourbigbook-web-profile-picture-upload). OurBigBook Web profile picture upload**. Clicking on the current profile picture opens up a file dialog which allows you to select an image from your computer to be your new profile picture.

<a id="_169"></a>
Announcements:<a id="_170"></a>

<a id="_171"></a>
- [https://x.com/OurBigBook/status/1868924960749826281](https://x.com/OurBigBook/status/1868924960749826281)
<a id="_172"></a>
- [https://mastodon.social/@ourbigbook/113667036536861645](https://mastodon.social/@ourbigbook/113667036536861645)
<a id="_173"></a>
- [https://www.linkedin.com/posts/ourbigbook_httpslnkdinexqfia-u-you-can-now-update-activity-7274690906065145856-1ho7/](https://www.linkedin.com/posts/ourbigbook_httpslnkdinexqfia-u-you-can-now-update-activity-7274690906065145856-1ho7/)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
