# Make rendered issue and comment fragments as short as possible

↑ **Parent:** [TODO](../todo-split.md)  
🏷️ **Tags:** [Comment](comment.md), [Web](web.md)

<a id="_300"></a>
For now I made them almost fully correct AFAIS:<a id="_301"></a>

<a id="_302"></a>
- no ID conflicts that would show on the same page, e.g. across issue IDs and comment IDs
<a id="_303"></a>
- links seem to go to where we want them to

<a id="_304"></a>
The only known bug is: [cannot link from comment to article](cannot-link-from-comment-to-article.md)

<a id="_305"></a>
However, in order to achieve this easily we used scopes liberally, and so the fragments are horrendously long.

<a id="_306"></a>
The ideal fragment setup for both comments and issues would be either:<a id="_307"></a>

<a id="_308"></a>
- we don't ever want to show multiple comments/issues from different issues on same page<a id="_309"></a>

  <a id="_310"></a>
  - issue IDs:<a id="_311"></a>

    <a id="_312"></a>
    - regular elements `my-header`
    <a id="_313"></a>
    - ToC IDs<a id="_314"></a>

      <a id="_315"></a>
      - the ToC: `_toc`
      <a id="_316"></a>
      - the links: `_toc/my-header`
  <a id="_317"></a>
  - comment IDs:<a id="_318"></a>

    <a id="_319"></a>
    - regular elements `_comment/1/my-header`
    <a id="_320"></a>
    - ToC IDs<a id="_321"></a>

      <a id="_322"></a>
      - the ToC: `_comment/1/_toc`
      <a id="_323"></a>
      - the links: `_comment/1/_toc/my-header`
<a id="_324"></a>
- we want to show multiple comments/issues from different issues on same page:<a id="_325"></a>

  <a id="_326"></a>
  - issue IDs:<a id="_327"></a>

    <a id="_328"></a>
    - regular elements `_issue/barack-obama/article-topic/1/my-header`
    <a id="_329"></a>
    - ToC IDs<a id="_330"></a>

      <a id="_331"></a>
      - the ToC: `_issue/barack-obama/article-topic/1/_toc`
      <a id="_332"></a>
      - the links: `_issue/barack-obama/article-topic/1/_toc/my-header`
  <a id="_333"></a>
  - comment IDs:<a id="_334"></a>

    <a id="_335"></a>
    - regular elements `_comment/barack-obama/article-topic/<issue-id>/<comment-id>/my-header`
    <a id="_336"></a>
    - ToC IDs<a id="_337"></a>

      <a id="_338"></a>
      - the ToC: `_comment/barack-obama/article-topic/<issue-id>/<comment-id>/_toc`
      <a id="_339"></a>
      - the links: `_comment/barack-obama/article-topic/<issue-id>/<comment-id>/_toc/my-header`

## ↑ Ancestors (2)

1. [TODO](../todo-split.md)
2. [OurBigBook Project](../split.md)
