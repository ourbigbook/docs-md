# Table of contents JavaScript open close interaction

↑ **Parent:** [Table of contents](table-of-contents.md)

To the left of table of content entries you can click on an open/close icon to toggle the visibility of different levels of the table of contents.

The main use case covered by the expansion algorithm is as follows:
- the page starts with all nodes open to facilitate Ctrl + F queries
- if you click on a node in that sate, you close all its children, to get a summarized overview of the contents
- if you click one of those children, it opens only its own children, so you can interactively continue exploring the tree

The exact behaviour is:
- the clicked node is open:
  - state 1 all children are closed. Action: open all children recursively, which puts us in state 2
  - state 2: not all children are closed. Action close all children, which puts us in state 1. This gives a good overview of the children, without any children of children getting in the way.
- state 3: the clicked node is closed (not showing any children). Action: open it to show all direct children, but not further descendants (i.e. close those children). This puts us in state 1.

Note that those rules make it impossible to close a node by clicking on it, the only way to close a node os to click on its parent, the state transitions are:
- 3 -\> 1
- 1 -\> 2
- 2 -\> 1
but we feel that it is worth it to do things like this to cover the main use case described above without having to add two buttons per entry.

Clicking on the link from a [header](header.md) up to the table of contents also automatically opens up the node for you in case it had been previously closed manually.

## ↑ Ancestors (5)

1. [Table of contents](table-of-contents.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
