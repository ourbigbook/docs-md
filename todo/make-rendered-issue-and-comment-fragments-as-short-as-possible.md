# Make rendered issue and comment fragments as short as possible

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Comment](comment.md), [Web](web.md)

For now I made them almost fully correct AFAIS:
- no ID conflicts that would show on the same page, e.g. across issue IDs and comment IDs
- links seem to go to where we want them to

The only known bug is: [cannot link from comment to article](cannot-link-from-comment-to-article.md)

However, in order to achieve this easily we used scopes liberally, and so the fragments are horrendously long.

The ideal fragment setup for both comments and issues would be either:
- we don't ever want to show multiple comments/issues from different issues on same page
  - issue IDs:
    - regular elements `my-header`
    - ToC IDs
      - the ToC: `_toc`
      - the links: `_toc/my-header`
  - comment IDs:
    - regular elements `_comment/1/my-header`
    - ToC IDs
      - the ToC: `_comment/1/_toc`
      - the links: `_comment/1/_toc/my-header`
- we want to show multiple comments/issues from different issues on same page:
  - issue IDs:
    - regular elements `_issue/barack-obama/article-topic/1/my-header`
    - ToC IDs
      - the ToC: `_issue/barack-obama/article-topic/1/_toc`
      - the links: `_issue/barack-obama/article-topic/1/_toc/my-header`
  - comment IDs:
    - regular elements `_comment/barack-obama/article-topic/<issue-id>/<comment-id>/my-header`
    - ToC IDs
      - the ToC: `_comment/barack-obama/article-topic/<issue-id>/<comment-id>/_toc`
      - the links: `_comment/barack-obama/article-topic/<issue-id>/<comment-id>/_toc/my-header`

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
