# Allow `{parent}` to point to `{file}` header

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [File](file.md)

<a id="_122"></a>
```
= my/file.txt

= Asdf
{parent=my/file.txt}
{parentFile}
```

<a id="_123"></a>
Same for tags.

<a id="_124"></a>
Currently there is some confusion in the code on treating the `<>{file}` like the file in `= Header{file}`: one if about pointing to things, the other is about the current thing. We will disambiguate with `parentFile`.

<a id="_125"></a>
Same for `tag` and `tagFile`.

<a id="_126"></a>
It is currently possible however to just do:<a id="_127"></a>

```
= .gitignore

= child
{parent=_file/.gitignore}
```
I need to think why it works.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
