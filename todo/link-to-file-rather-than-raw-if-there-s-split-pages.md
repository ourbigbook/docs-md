<h1 id="link-to-file-rather-than-raw-if-there-s-split-pages">Link to _file rather than _raw if there's split pages</h1>

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [File autogen](file-autogen.md)

<a id="_15"></a>
E.g.:<a id="_16"></a>

```
= path/to/myfile.txt
{file}
```
would generate a breadcrumb like:<a id="_17"></a>

```
(root)/path/to/<myfile.txt>{file}{split}
```
where `{split}` is a possibly new argument that ensures it links to split if there are split pages, and not the current:<a id="_18"></a>

```
(root)/path/to/\a[myfile.txt]
```
This would make [file autogen](file-autogen.md) much more useful and visible. The general premise is that we should link to split `{file}` preferentially always.

<a id="_19"></a>
Pre-requisite: [Allow linking to auto-generated files](allow-linking-to-auto-generated-files.md)

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
