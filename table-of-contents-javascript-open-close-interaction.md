# Table of contents JavaScript open close interaction

↑ **Parent:** [Table of contents](table-of-contents.md)

To the left of table of content entries you can click on an open/close icon to toggle the visibility of different levels of the table of contents.

The main use case covered by the expansion algorithm is as follows:
- the page starts with all nodes open to facilitate Ctrl + F queries
- if you click an open node, you close its direct branches to get a summarized overview of its contents
- you can then click it again to close the node itself
- clicking a closed node opens its entire subtree, after which you can summarize it again

The exact behaviour is:
- summarized: the clicked node is open and every direct child is either closed or has no children. Action: close the clicked node
- closed: the clicked node is not showing its children. Action: open the clicked node and all its descendants recursively
- any other open state, including a fully open or mixed subtree. Action: summarize it by closing every direct child that has children

The main cycle is therefore: summarized -\> closed -\> fully open -\> summarized.

Clicking on the link from a [header](header.md) up to the table of contents also automatically opens up the node for you in case it had been previously closed manually.

## ↑ Ancestors (5)

1. [Table of contents](table-of-contents.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
