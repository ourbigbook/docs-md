# Allow `{parent}` to point to `{file}` header

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [File](file.md)

```
= my/file.txt

= Asdf
{parent=my/file.txt}
{parentFile}
```

Same for tags.

Currently there is some confusion in the code on treating the `<>{file}` like the file in `= Header{file}`: one if about pointing to things, the other is about the current thing. We will disambiguate with `parentFile`.

Same for `tag` and `tagFile`.

It is currently possible however to just do:
```
= .gitignore

= child
{parent=-/file/.gitignore}
```
I need to think why it works.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
