# Allow linking to auto-generated files

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [File autogen](file-autogen.md)

It would be cool if we could do:
```
<myfile.txt>{file}
```
when there is a file `myfile.txt` without a corresponding `{file}` header such as:
```
= myfile.txt
{file}
```
As of writing, on static we already autogenerate such `-/file` pages for all files (not yet on web but we should too), so it's just a matter of checking if the target file exists when the ID doesn't for error checking, and linking to the \_file.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Link to \_file rather than \_raw if there's split pages](link-to-file-rather-than-raw-if-there-s-split-pages.md)
