# The ID of the first header is derived from the filename

↑ **Parent:** [The toplevel header](the-toplevel-header.md)

With the exception of  For example:

When the OurBigBook input comes from a file (and not e.g. [stdin](stdin-conversion.md)), the default ID of the first header in the document is derived from the basename of the OurBigBook input source file rather than from its title.

The only exception to this is [the home article](the-home-article.md), where the ID is empty.

For example, in file named `my-file.bigb` which contains:
```
= Awesome ourbigbook file
```
the ID of the header is `my-file` rather than `awesome-ourbigbook-file`. See also: [automatic ID from title](automatic-id-from-title.md).

If the file is an [index file](index-file.md) other than [the toplevel index file](the-toplevel-index-file.md), then the basename of the parent directory is used instead, e.g. the toplevel ID of a file:
```
my-subdir/index.bigb
```
would be:
```
#my-subdir
```
rather than:
```
#index.bigb
```

For the toplevel index file however, the ID is just taken from the header itself as usual. This is done because you often can't general control the directory name of a project.

For example, a [GitHub pages](publish-target-github-pages.md) root directory must be named as `<username>.github.io`. And users may need to rename directories to avoid naming conflicts.

As a consequence of this, the toplevel index file cannot [be included in other files](include.md).

TODO: we kind of wanted this to be the ID of the toplevel header instead of the first header, but this would require an extra postprocessing pass (to determine if the first header is toplevel or not), which might affect performance, so we are not doing it right now.

## ↑ Ancestors (5)

1. [The toplevel header](the-toplevel-header.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Automatic ID from title](automatic-id-from-title.md)
- [Include](include.md)
