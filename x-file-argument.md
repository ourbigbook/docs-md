# `\x` `file` argument

↑ **Parent:** [`\x` arguments](x-arguments.md)

Allows to link to [headers](header.md) with the [`\H` `file` argument](h-file-argument.md), e.g.:
```
= My header

Check out this amazing file: <path/to/myfile.txt>{file}

== path/to/myfile.txt
```

Some live demos follow:
```
\x[file_demo]{file}
```
which renders as:



> [file_demo](_file/file_demo.md)


```
\x[file_demo/file_demo_subdir]{file}
```
which renders as:



> [file_demo/file_demo_subdir](_file/file_demo/file_demo_subdir.md)


```
\x[file_demo/file_demo_subdir/hello_world.js]{file}
```
which renders as:



> [file_demo/file_demo_subdir/hello_world.js](_file/file_demo/file_demo_subdir/hello_world.js.md)


```
\x[file_demo/my.bin]{file}
```
which renders as:



> [file_demo/my.bin](_file/file_demo/my.bin.md)


```
\x[Tank_man_standing_in_front_of_some_tanks.jpg]{file}
```
which renders as:



> [Tank_man_standing_in_front_of_some_tanks.jpg](_file/Tank_man_standing_in_front_of_some_tanks.jpg.md)


```
\x[https://www.youtube.com/watch?v=YeFzeNAHEhU]{file}
```
which renders as:



> [https://www.youtube.com/watch?v=YeFzeNAHEhU](_file/https:/www.youtube.com/watch?v=YeFzeNAHEhU.md)

## ↑ Ancestors (5)

1. [`\x` arguments](x-arguments.md)
2. [Internal link](internal-link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`\H` `file` argument](h-file-argument.md)
