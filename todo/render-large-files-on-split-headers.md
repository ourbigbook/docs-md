# Render large files on split headers

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [File](file.md)

<a id="_440"></a>
Currently files that are large don't render in either multi nor split headers.

<a id="_441"></a>
But instead we want it to render on split headers because the \_raw version does not always show on GitHub pages, but rather gets downloaded which is bad.

<a id="_442"></a>
The `{file}` version is also cool as it allows easy navigation to other files, and comments to be added.

<a id="_443"></a>
This is currently not so easy to implement because things are done at the ast tree level rather than at render time, which is bad. So the same ast ends up going for both split and nosplit renders.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
