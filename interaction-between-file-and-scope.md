# Interaction between `{file}` and `{scope}`

↑ **Parent:** [`\H` `file` argument](h-file-argument.md)

IDs defined under `_file/path/to/myfile.txt.bigb` don't have any scope, e.g.:
```
= myfile.txt
{file}

\Image[dog.png]
{title=dog}
```
would simply have ID `image-dog`.

Headers marked with the [`\H` `file` argument](h-file-argument.md) never have any scope e.g. in:
```
= Toplevel

== My scope
{scope}

=== myfile.txt
{file}
```
the [ID](element-id.md) of the third header is just:
```
_file/myfile.txt
```
and not:
```
my-scope/_file/myfile.txt
```
or:
```
_file/my-scope/myfile.txt
```
This is because a `{file}` header is already fully specified by its position in the tree or the given URL, so it doesn't make much sense to add more to it.

## ↑ Ancestors (6)

1. [`\H` `file` argument](h-file-argument.md)
2. [`\H` arguments](h-arguments.md)
3. [Header](header.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)
