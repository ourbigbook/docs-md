# Project banner

↑ **Parent:** [Project identity](project-identity.md)

<a id="image-topics-page-banner"></a>
![](https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/banner-topics-signed-in-800.png)

**[Figure 95](#image-topics-page-banner). Topics page banner**. Initial project banner showing the [OurBigBook Web topics](ourbigbook-web-topics.md) feature. Not very subtle, but will do as a placeholder.

The downside of this is that much of its bottom left is hidden by the profile picture on websites such as Twitter and LinkedIn.

The banner is also a bit narrow for certain websites, and either looks rescaled, or is outright not allowd with editing, e.g. YouTube requires a minium width of 1024, with 2048 recommended.

YouTube is also extremelly picky and hard to make the banner look right as it reserves mandatory huge height for TV displays! The best approach we can find is to make the image huge and fill in black with:
```
convert banner-topics-signed-in-800.png -background black -gravity center -extent 2000x1000 tmp.png
```
and then drag the image selection so that the desktop view covers the area we care about.

---

Websites that accept banners:
- Twitter
- LinkedIn
- YouTube
- Reddit
- Patreon
- Facebook

## ↑ Ancestors (4)

1. [Project identity](project-identity.md)
2. [Publicity](publicity.md)
3. [Developing OurBigBook](developing-ourbigbook.md)
4. [OurBigBook Project](split.md)
