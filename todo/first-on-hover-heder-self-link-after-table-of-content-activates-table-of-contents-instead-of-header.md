# First on-hover heder self link after table of content activates table of contents instead of header 

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Web](web.md)

<a id="_673"></a>
E.g.: [https://cirosantilli.com/physics#how-to-teach-and-learn-physics](https://cirosantilli.com/physics#how-to-teach-and-learn-physics)

<a id="_674"></a>
Broken ToC HTML render?

<a id="_675"></a>
OK, understood the root cause: we moved to rendering the ToC from inside the H rendering function itself, and as a result there is a single toplevel\_child\_modifier which acts on that entire output.

<a id="_676"></a>
We'll need to create something more custom to properly handle this case.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
