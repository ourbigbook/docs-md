# Internal link title link removal

↑ **Parent:** [Cross file internal link](cross-file-internal-link.md)

If the target `title` argument contains a link from either another [internal links](internal-link.md) or a regular [external hyperlink](link.md), OurBigBook automatically prevents that link from rendering as a link when no explicit body is given.

This is done because [nested links are illegal in HTML](https://stackoverflow.com/questions/9882916/are-you-allowed-to-nest-a-link-inside-of-a-link), and the result would be confusing.

This use case is most common when dealing with media such as [images](image.md). For example in:
```
= afds

\x[image-aa-zxcv-lolol-bb]

== qwer

\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{title=aa \x[zxcv][zxcv] \a[http://example.com][lolol] bb}

== zxcv
```
the `\x[image-aa-zxcv-lolol-bb]` renders something like:
```
<a href="#image-aa-zxcv-lolol-bb">aa zxcv lolol bb</a>
```
and not:
```
<a href="#image-aa-zxcv-lolol-bb">aa <a href="zxcv">zxcv</a> <a href="http://example.com">lolol</a> bb</a>
```

Live example:
```
This is a nice image: \x[image-aa-zxcv-lolol-bb].

\Image[Tank_man_standing_in_front_of_some_tanks.jpg]
{title=aa \x[internal-link-title-link-removal][zxcv] \a[http://example.com][lolol] bb}
```
which renders as:



> This is a nice image: [Figure 46. "aa zxcv lolol bb"](#image-aa-zxcv-lolol-bb).
> 
> <a id="image-aa-zxcv-lolol-bb"></a>
> ![](_raw/Tank_man_standing_in_front_of_some_tanks.jpg)
> 
> **[Figure 46](#image-aa-zxcv-lolol-bb). aa zxcv lolol bb**.

## ↑ Ancestors (5)

1. [Cross file internal link](cross-file-internal-link.md)
2. [Internal link](internal-link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
