# Image title with x to image with content incorrectly disallowed

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Lib](lib.md)

<a id="_63"></a>
Should only blow up if the `\\x` does not have a content explicitly set. See broken test `cross reference from image title to previous non-header with content is allowed`.

<a id="_64"></a>
To fix we need to store some extra data on the Ref or Id table that determines if the reference needs the title or not to determine its own ID.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [`\x` within `title` restrictions](../x-within-title-restrictions.md)
