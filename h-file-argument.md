# `\H` `file` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)

If given, the current section contains metadata about file or other resource with the given URL.

<a id="image-ourbigbook-file-feature"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/file.png" alt="" height="785">

**[Figure 23](#image-ourbigbook-file-feature). OurBigBook file feature**. [Source](https://cirosantilli.com/\_dir/nodejs/).

If empty, the URL of the file is extracted directly from the header. Otherwise, the given URL is used.

for example:
```
= path/to/myfile.c
{file}

An explanation of what this file is about.
```
renders a bit like:
```
= path/to/myfile.c
{id=_file/path/to/myfile.c}

An explanation of what this file is about.

\a[path/to/myfile.c]

``
// Contents of path/to/myfile.c
int main() {
  return 1;
}
``
```
so note how:
- [automatic ID from title](automatic-id-from-title.md) does not normalize the path, e.g. it does not convert `/` to `-`.

  Also, a [`_file/` prefix](file-output-directory.md) is automatically added to the ID. This is needed with [`-S`, `--split-headers`](split-headers.md) to avoid a collision between:
  - `path/to/myfile.c`: the actual file
  - `_file/path/to/myfile.c`: the metadata about that file. Note that locally the `.html` extension is added as in `file/path/to/myfile.c.html` which avoids the collision. But on a server deployment, the `.html` is not present, and there would be a conflict if we didn't add that `file/` prefix.
- a link to the is added automatically, since users won't be able to click it from the header, as clicking on the header will just link to the header itself
- a preview is added. The type of preview is chosen as follows:
  - if the URL has an image extension, do an [image](image.md) preview
  - otherwise if the URL has a video extension, or is a YouTube URL, do a [video](video.md) preview
  - otherwise, don't show a preview, as we don't know anything sensible to show

In some cases however, especially when dealing with external URLs, we might want to have a more human readable title with a non empty `file` argument:
```
The video \x[tank-man-by-cnn-1989] is very useful.

= Tank Man by CNN (1989)
{c}
{file=https://www.youtube.com/watch?v=YeFzeNAHEhU}

An explanation of what this video is about.
```
which renders something like:
```
The video \x[tank-man-by-cnn-1989] is very useful.

= Tank Man by CNN (1989)
{id=_file/https://www.youtube.com/watch?v=YeFzeNAHEhU}

\Video[https://www.youtube.com/watch?v=YeFzeNAHEhU]

An explanation of what this video is about.
```

To make [internal links](internal-link.md) to `{file}` headers, use the [`\x` `file` argument](x-file-argument.md).

**Table of contents**

- [`\H` `file` argument toplevel header](h-file-argument-toplevel-header.md)
- [Interaction between `{file}` and `{scope}`](interaction-between-file-and-scope.md)
- [`_file` input directory](file-input-directory.md)
- [`\H` `file` argument demo](h-file-argument-demo.md)
  - [file\_demo](_file/file_demo.md)
  - [file\_demo/file\_demo\_subdir](_file/file_demo/file_demo_subdir.md)
  - [file\_demo/hello\_world.js](_file/file_demo/hello_world.js.md)
  - [file\_demo/file\_demo\_subdir/hello\_world.js](_file/file_demo/file_demo_subdir/hello_world.js.md)
  - [index.js](_file/index.js.md)
  - [file\_demo/my.bin](_file/file_demo/my.bin.md)
  - [Tank\_man\_standing\_in\_front\_of\_some\_tanks.jpg](_file/Tank_man_standing_in_front_of_some_tanks.jpg.md)
  - [Tank Man by CNN (1989)](_file/https:/www.youtube.com/watch?v=YeFzeNAHEhU.md)
  - [https://example.com](_file/https:/example.com.md)

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (11)

- [OurBigBook Project](split.md)
- [Features](features.md)
- [`_file` output directory](file-output-directory.md)
- [`\H` `file` argument](h-file-argument.md)
- [`\H` `file` argument demo](h-file-argument-demo.md)
- [`\H` `file` argument toplevel header](h-file-argument-toplevel-header.md)
- [Interaction between `{file}` and `{scope}`](interaction-between-file-and-scope.md)
- [Always show large text files on `_file` split headers](news/always-show-large-text-files-on-file-split-headers.md)
- [Automatically create `_file` pages for every file](news/automatically-create-file-pages-for-every-file.md)
- [File](todo/file.md)
- [`\x` `file` argument](x-file-argument.md)
