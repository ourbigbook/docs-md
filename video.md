# Video

↑ **Parent:** [Macro](macro.md)

Very analogous to [images](image.md), only differences will be documented here.

In the case of videos, [where to store images](where-to-store-images.md) becomes even more critical since videos are even larger than images, such that the following storage approaches are impractical off the bat:
- [store images inside the repository itself](store-images-inside-the-repository-itself.md)
- [store images in a separate media repository](store-images-in-a-separate-media-repository.md)
As a result, then [Wikimedia Commons](https://commons.wikimedia.org) is one of the best options [much like for images](store-images-in-wikimedia-commons.md):
```
\Video[https://upload.wikimedia.org/wikipedia/commons/8/85/Vacuum_pump_filter_cut_and_place_in_eppendorf.webm]
{id=sample-video-in-wikimedia-commons}
{title=Nice sample video stored in Wikimedia Commons}
{start=5}
```
which renders as:



> <a id="sample-video-in-wikimedia-commons"></a>
> **[Video 6](#sample-video-in-wikimedia-commons). Nice sample video stored in Wikimedia Commons.** [Source](https://commons.wikimedia.org/wiki/File:Vacuum_pump_filter_cut_and_place_in_eppendorf.webm).

We also handle more complex transcoded video URLs just fine:
```
\Video[https://upload.wikimedia.org/wikipedia/commons/transcoded/1/19/Scientific_Industries_Inc_Vortex-Genie_2_running.ogv/Scientific_Industries_Inc_Vortex-Genie_2_running.ogv.480p.vp9.webm]
{id=sample-video-in-wikimedia-commons-transcoded}
{title=Nice sample video stored in Wikimedia Commons transcoded}
```
which renders as:



> <a id="sample-video-in-wikimedia-commons-transcoded"></a>
> **[Video 7](#sample-video-in-wikimedia-commons-transcoded). Nice sample video stored in Wikimedia Commons transcoded.** [Source](https://commons.wikimedia.org/wiki/File:Scientific_Industries_Inc_Vortex-Genie_2_running.ogv).

Commons is better than YouTube if your content is on-topic there because:
- they have no ads
- it allows download of the videos: [https://www.quora.com/Can-I-download-Creative-Commons-licensed-YouTube-videos-to-edit-them-and-use-them](https://www.quora.com/Can-I-download-Creative-Commons-licensed-YouTube-videos-to-edit-them-and-use-them).
- it makes it easier for other users to find and re-use your videos

If your video does not fit the above Wikimedia Commons requirements, YouTube could be a good bet. OurBigBook [automatically detects YouTube URLs](https://github.com/ourbigbook/ourbigbook/issues/50) for you, so the following should just work:
```
\Video[https://youtube.com/watch?v=YeFzeNAHEhU&t=38]
{id=sample-video-from-youtube-implicit-youtube}
{title=Nice sample video embedded from YouTube implicit from `youtube.com` URL}
```
which renders as:



> <a id="sample-video-from-youtube-implicit-youtube"></a>
> **[Video 8](#sample-video-from-youtube-implicit-youtube). Nice sample video embedded from YouTube implicit from `youtube.com` URL.** [Source](https://youtube.com/watch?v=YeFzeNAHEhU&amp;t=38).

The `youtu.be` domain hack URLs also work;
```
\Video[https://youtu.be/YeFzeNAHEhU?t=38]
{id=sample-video-from-youtube-implicit-youtu-be}
{title=Nice sample video embedded from YouTube implicit from `youtu.be` URL}
```
which renders as:



> <a id="sample-video-from-youtube-implicit-youtu-be"></a>
> **[Video 9](#sample-video-from-youtube-implicit-youtu-be). Nice sample video embedded from YouTube implicit from `youtu.be` URL.** [Source](https://youtu.be/YeFzeNAHEhU?t=38).

Alternatively, you can reach the same result in a more explicit and minimal way by setting `{provider=youtube}` and the [`start`](video-start-argument.md) arguments:
```
\Video[YeFzeNAHEhU]{provider=youtube}
{id=sample-video-from-youtube-explicit}
{title=Nice sample video embedded from YouTube with explicit `youtube` argument}
{start=38}
```
which renders as:



> <a id="sample-video-from-youtube-explicit"></a>
> **[Video 10](#sample-video-from-youtube-explicit). Nice sample video embedded from YouTube with explicit `youtube` argument.** [Source](https://youtube.com/watch?v=YeFzeNAHEhU).

When the `youtube` provider is selected, the Video address should only to contain the YouTube video ID, which shows in the YouTube URL for the video as:
```
https://www.youtube.com/watch?v=<video-id>
```
Remember that you can also enable the `youtube` provider by default on your [`ourbigbook.json`](ourbigbook-json.md) with:
```
"media-provider" {
  "youtube": {"default-for": "video"}
}
```

But you can also use raw video files from any location that can serve them of course, e.g. here is one stored in this repository: [Video 11. "Nice sample video stored in this repository"](#sample-video-in-repository).
```
\Video[Tank_man_side_hopping_in_front_of_some_tanks.mp4]
{id=sample-video-in-repository}
{title=Nice sample video stored in this repository}
{source=https://www.youtube.com/watch?v=YeFzeNAHEhU}
{start=3}
```
which renders as:



> <a id="sample-video-in-repository"></a>
> **[Video 11](#sample-video-in-repository). Nice sample video stored in this repository.** [Source](https://www.youtube.com/watch?v=YeFzeNAHEhU).

And as for images, setting `titleFromSrc` automatically calculates a title for you:
```
\Video[Tank_man_side_hopping_in_front_of_some_tanks.mp4]
{titleFromSrc}
{source=https://www.youtube.com/watch?v=YeFzeNAHEhU}
```
which renders as:



> <a id="video-tank-man-side-hopping-in-front-of-some-tanks"></a>
> **[Video 12](#video-tank-man-side-hopping-in-front-of-some-tanks). Tank man side hopping in front of some tanks.** [Source](https://www.youtube.com/watch?v=YeFzeNAHEhU).

**Table of contents**

- [Video lazy loading](video-lazy-loading.md)
- [`\Video` argument](video-argument.md)
  - [`\Video` `description` argument](video-description-argument.md)
  - [`\Video` `title` argument](video-title-argument.md)
  - [`\Video` `start` argument](video-start-argument.md)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [`\H` `file` argument](h-file-argument.md)
- [`\H` `splitDefault` argument](h-splitdefault-argument.md)
- [`Media-providers`](ourbigbook-json/media-providers.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
