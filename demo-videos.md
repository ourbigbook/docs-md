# Demo videos

↑ **Parent:** [Publicity](publicity.md)

Demo videos are uploaded to the [official YouTube account](official-accounts.md): [https://www.youtube.com/@OurBigBook](https://www.youtube.com/@OurBigBook)

The video files together with the assets used to make them are also made available in the [OurBigBook media repository](ourbigbook-media-repository.md) under the [`video/` directory](https://github.com/ourbigbook/ourbigbook-media/tree/master/video).

Video guidelines:
- desktop recording area size: 720x720. This could perhaps be optimized, but this is a reasonable size that works both as an YouTube Short and Twitter post.

  Previously we had been using 700x700, but at some point YouTube appears to have stopped generating 720p resolution for those, and 480p is just too bad.

  We've been happily using vokoscreenNG.

  A good technique is to move the recording window to the lower left bottom of the screen, which stops things from floating around too much.
- use Chromium/Chrome to record
- resize window to fit recording area horizontally by using the Ctrl + Shift + C debugger view. Make sure to also resize the browser window vertically (cannot be done on debugger, needs resizing actual window) otherwise you won't be able to scroll if the page is not taller than the viewport.
- be careful about single pixel black border lines straying in the recording area, they are mega visible against the clear chrome browser bar on the finished output!
- music style guidelines: cool, beats, techno, mysterious, upbeat

  Some of the videos contain non-fully free YouTube music added via the YouTube UI. Reupload together with the video files appears however allowed. Ideally we should use fully [CC BY-SA](https://ourbigbook.com/go/topic/cc-by-sa) music, but it is quite hard to find good ones. NC is not acceptable.
- hardcode subtitles in the video. No voice. Previously we were using Aegisub to create the subtitles in `.ass` format and ffmpeg to hardcode:
  ```
  ffmpeg -i raw.mkv -vf subtitles=sub.ass out.mkv
  ```

  but later we [learnt about KDenlive support for subtitles](https://www.youtube.com/watch?v=1yuc60lz2Us) and moved to that instead as it is even more convenient to have it all in one place. Use:
  - 22pt white font with black background to improve readability
  - aim to have 3/4 lines of subtitle maximum per frame

  When recording, make sure that all key mouse action happens on the top half of the viewport, otherwise it will get covered by the subtitles in downstream editing.
- on YouTube, add the video as the first video of the "Videos" playlist: [https://www.youtube.com/playlist?list=PLshTOzrBHLkZlpvTuBdphKLWwU7xBV6VF](https://www.youtube.com/playlist?list=PLshTOzrBHLkZlpvTuBdphKLWwU7xBV6VF) This list is needed because otherwise YouTube's stupid "Shorts" features produces two separate timelines by default, one for shorts and one for non-shorts. With this list, all videos can be seen easily as non-shorts.

## ↑ Ancestors (3)

1. [Publicity](publicity.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)
