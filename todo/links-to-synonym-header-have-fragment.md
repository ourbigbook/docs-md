# Links to synonym header have fragment

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Bug](bug.md), [Web](web.md)

E.g. from [https://ourbigbook.com/cirosantilli/ciro-santilli](https://ourbigbook.com/cirosantilli/ciro-santilli):
```
<Python>
```
renders as:
```
/cirosantilli/python-programming-language#cirosantilli/python-programming-language
```
instead of the desired:
```
/cirosantilli/python-programming-language
```

However the link to the non-synonym header:
```
<Python (programming language)>
```
renders correctly without the fragment

OK, this was also reproducible on CLI, links to toplevel synonyms had fragments, just it is infinitely more visible on web where everything is toplevel.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
