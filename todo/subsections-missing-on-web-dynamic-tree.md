# Subsections missing on web dynamic tree

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Bug](bug.md), [Dynamic tree fetch](dynamic-tree-fetch.md)

Going to close it for now as irreproducible. Worked around it by fixing data manualy with the new `nested-set` CLI tool. Will try to debug further if it shows up again in the future.

On web now:
- [https://ourbigbook.com/barack-obama](https://ourbigbook.com/barack-obama) shows Fundamental theorem of calculus under "Integral", correct
- [https://ourbigbook.com/barack-obama/mathematics](https://ourbigbook.com/barack-obama/mathematics) does not show "Fundamental theorem of calculus", incorrect

We can only reproduce locally by copying the database, we haven't managed to reach such state by a clean sequence of pure API calls, clean naive `web/bin/generate-demo-data -C -u1` didn't reproduce either.

Upon quickly inspectig the DB we see that the nested set indexes are wrong:
```
[ 'barack-obama', 0, 36 ],
[ 'barack-obama/mathematics', 1, 9 ],
[ 'barack-obama/fundamental-theorem-of-calculus', 9, 11 ],
```
`barack-obama/mathematics` should stop something larger than `9` to include `barack-obama/fundamental-theorem-of-calculus` and other children.

The question is now if this is still reachable, of if it was due to a previous bug.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
