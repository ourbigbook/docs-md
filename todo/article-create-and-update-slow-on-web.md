# Article create and update slow on web

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Performance](performance.md), [Web](web.md)

<a id="_596"></a>
[https://ourbigbook.com/api/articles](https://ourbigbook.com/api/articles)

<a id="_597"></a>
For user cirosantilli, just pushed cirosantilli.github.io at aa60ccb934bf9646d548e6b761489d31aec1a341, which has almost 7k articles.

<a id="_598"></a>
The POST to [https://ourbigbook.com/api/articles](https://ourbigbook.com/api/articles) is taking about 3s to 4s on ourbigbook.com "Waiting for server response", 3.44s seems like an common average exact value that often comes back.

<a id="_599"></a>
This was after dynamic article tree, one suspicion is that it might be linked to maintaining the nested set state on a large set of articles. I really hope that's not it, as it would be hard to fix.

<a id="_600"></a>
Doing it from the `barack-obama` test user which only has about 50 articles leads to the same result, but we believe it is because we are not indexing things by user properly (this was added later), so might still be due to nested set.

<a id="_601"></a>
Locally on sqlite is only 800 ms to 900 ms.

<a id="_602"></a>
Locally on postgresql with `barack-obama` user and no `cirosantilli` data, the POST is almost instantaneous however... 100ms or less!

<a id="_603"></a>
Local postgresql with `cirosantilli` user after uploading cirosantilli.github.io with about 7k articles: usually around 2.4s, sometimes a bit less.

<a id="_604"></a>
Same but with `barack-obama`: 2.16s! So the main slowdown is likely that we are not properly indexing things, as one users' article affects the other's!

<a id="_605"></a>
Let's hack it up to see:<a id="_606"></a>

```
./bin/psql
alter table "Article" add "authorId" integer;
update "Article" as a set "authorId" = f."authorId" from "File" as f where a."fileId" = f.id
create index idx_nested ON "Article" using btree ("authorId", "nestedSetIndex");
```

<a id="_607"></a>
and patch:

<a id="_608"></a>
```
diff --git a/web/convert.js b/web/convert.js
index 59870ae3..ff834708 100644
--- a/web/convert.js
+++ b/web/convert.js
@@ -568,6 +568,7 @@ async function convertArticle({
         const rendered_output = extra_returns.rendered_outputs[outpath]
         const renderFull = rendered_output.full
         articleArgs.push({
+          authorId: file.authorId,
           depth: newDepth,
           fileId: file.id,
           h1Render: renderFull.substring(0, rendered_output.h1RenderLength),
@@ -599,6 +600,7 @@ async function convertArticle({
         articleArgs,
         {
           updateOnDuplicate: [
+            'authorId',
             'h1Render',
             'h2Render',
             'titleRender',
diff --git a/web/models/article.js b/web/models/article.js
index 40dbbdba..1c382acc 100644
--- a/web/models/article.js
+++ b/web/models/article.js
@@ -13,6 +13,10 @@ module.exports = (sequelize) => {
     'Article',
     {
       // E.g. `johnsmith/mathematics`.
+      authorId: {
+        type: DataTypes.INTEGER,
+        allowNull: false,
+      },
       slug: {
         type: DataTypes.TEXT,
         unique: {
```

<a id="_609"></a>
Didin't help :-(

<a id="_610"></a>
A cleaner benchmarking can now be done with:<a id="_611"></a>

```
OURBIGBOOK_POSTGRES=1 ./bin/generate-demo-data.js -C -u1 -a650 -i0 -c0
```
By this size, things are already unreasonably slow, and you can visibly see the latter renders being much slower than the early ones. We can then do a very minimal one off benchmark of a single slow article update with:<a id="_612"></a>

```
OURBIGBOOK_POSTGRES=1 ./bin/generate-demo-data.js -u1 -a1 -i0 -c0
```
OK, now the test case is clearer.

<a id="_613"></a>
By also enabling SQL logging:<a id="_614"></a>

```
time DEBUG='*:sql:*' OURBIGBOOK_POSTGRES=1 ./bin/generate-demo-data.js -u1 -a1 -i0 -c0
```
which gave:<a id="_615"></a>

```
real    0m1.400s
user    0m0.643s
sys     0m0.068s
```
we will be able to see any slow queries. We reach the following two massively slow queries:<a id="_616"></a>

```
SELECT
  "Ref".*,
  "to"."id" AS "to.id",
  "to"."idid" AS "to.idid",
  "to"."path" AS "to.path",
  "to"."toplevel_id" AS "to.toplevel_id",
  "to"."ast_json" AS "to.ast_json",
  "to"."macro_name" AS "to.macro_name",
  "to"."createdAt" AS "to.createdAt",
  "to"."updatedAt" AS "to.updatedAt",
  "to->File"."id" AS "to.File.id",
  "to->File"."path" AS "to.File.path",
  "to->File"."toplevel_id" AS "to.File.toplevel_id",
  "to->File"."last_parse" AS "to.File.last_parse",
  "to->File"."last_render" AS "to.File.last_render",
  "to->File"."titleSource" AS "to.File.titleSource",
  "to->File"."bodySource" AS "to.File.bodySource",
  "to->File"."createdAt" AS "to.File.createdAt",
  "to->File"."updatedAt" AS "to.File.updatedAt",
  "to->File"."authorId" AS "to.File.authorId",
  "to->File->file"."id" AS "to.File.file.id",
  "to->File->file"."slug" AS "to.File.file.slug",
  "to->File->file"."topicId" AS "to.File.file.topicId",
  "to->File->file"."titleRender" AS "to.File.file.titleRender",
  "to->File->file"."titleSource" AS "to.File.file.titleSource",
  "to->File->file"."titleSourceLine" AS "to.File.file.titleSourceLine",
  "to->File->file"."render" AS "to.File.file.render",
  "to->File->file"."h1Render" AS "to.File.file.h1Render",
  "to->File->file"."h2Render" AS "to.File.file.h2Render",
  "to->File->file"."depth" AS "to.File.file.depth",
  "to->File->file"."score" AS "to.File.file.score",
  "to->File->file"."nestedSetIndex" AS "to.File.file.nestedSetIndex",
  "to->File->file"."nestedSetNextSibling" AS "to.File.file.nestedSetNextSibling",
  "to->File->file"."createdAt" AS "to.File.file.createdAt",
  "to->File->file"."updatedAt" AS "to.File.file.updatedAt",
  "to->File->file"."fileId" AS "to.File.file.fileId",
  "from"."id" AS "from.id",
  "from"."idid" AS "from.idid",
  "from"."path" AS "from.path",
  "from"."toplevel_id" AS "from.toplevel_id",
  "from"."ast_json" AS "from.ast_json",
  "from"."macro_name" AS "from.macro_name",
  "from"."createdAt" AS "from.createdAt",
  "from"."updatedAt" AS "from.updatedAt",
  "from->File"."id" AS "from.File.id",
  "from->File"."path" AS "from.File.path",
  "from->File"."toplevel_id" AS "from.File.toplevel_id",
  "from->File"."last_parse" AS "from.File.last_parse",
  "from->File"."last_render" AS "from.File.last_render",
  "from->File"."titleSource" AS "from.File.titleSource",
  "from->File"."bodySource" AS "from.File.bodySource",
  "from->File"."createdAt" AS "from.File.createdAt",
  "from->File"."updatedAt" AS "from.File.updatedAt",
  "from->File"."authorId" AS "from.File.authorId",
  "from->File->file"."id" AS "from.File.file.id",
  "from->File->file"."slug" AS "from.File.file.slug",
  "from->File->file"."topicId" AS "from.File.file.topicId",
  "from->File->file"."titleRender" AS "from.File.file.titleRender",
  "from->File->file"."titleSource" AS "from.File.file.titleSource",
  "from->File->file"."titleSourceLine" AS "from.File.file.titleSourceLine",
  "from->File->file"."render" AS "from.File.file.render",
  "from->File->file"."h1Render" AS "from.File.file.h1Render",
  "from->File->file"."h2Render" AS "from.File.file.h2Render",
  "from->File->file"."depth" AS "from.File.file.depth",
  "from->File->file"."score" AS "from.File.file.score",
  "from->File->file"."nestedSetIndex" AS "from.File.file.nestedSetIndex",
  "from->File->file"."nestedSetNextSibling" AS "from.File.file.nestedSetNextSibling",
  "from->File->file"."createdAt" AS "from.File.file.createdAt",
  "from->File->file"."updatedAt" AS "from.File.file.updatedAt",
  "from->File->file"."fileId" AS "from.File.file.fileId"
FROM
  (
    SELECT
      "Ref"."id",
      "Ref"."type",
      "Ref"."from_id",
      "Ref"."to_id",
      "Ref"."defined_at",
      "Ref"."defined_at_line",
      "Ref"."defined_at_col",
      "Ref"."inflected",
      "Ref"."to_id_index",
      "Ref"."createdAt",
      "Ref"."updatedAt"
    FROM
      "Ref" AS "Ref"
    WHERE
      "Ref"."to_id" = '@barack-obama/test-data'
      AND "Ref"."type" = 0
    LIMIT
      1
  ) AS "Ref"
  LEFT OUTER JOIN "Id" AS "to" ON "Ref"."to_id" = "to"."idid"
  LEFT OUTER JOIN "File" AS "to->File" ON "to"."idid" = "to->File"."toplevel_id"
  LEFT OUTER JOIN "Article" AS "to->File->file" ON "to->File"."id" = "to->File->file"."fileId"
  LEFT OUTER JOIN "Id" AS "from" ON "Ref"."from_id" = "from"."idid"
  LEFT OUTER JOIN "File" AS "from->File" ON "from"."idid" = "from->File"."toplevel_id"
  LEFT OUTER JOIN "Article" AS "from->File->file" ON "from->File"."id" = "from->File->file"."fileId";

+451ms

SELECT
  "Id".*,
  "File"."id" AS "File.id",
  "File"."path" AS "File.path",
  "File"."toplevel_id" AS "File.toplevel_id",
  "File"."last_parse" AS "File.last_parse",
  "File"."last_render" AS "File.last_render",
  "File"."titleSource" AS "File.titleSource",
  "File"."bodySource" AS "File.bodySource",
  "File"."createdAt" AS "File.createdAt",
  "File"."updatedAt" AS "File.updatedAt",
  "File"."authorId" AS "File.authorId",
  "File->file"."id" AS "File.file.id",
  "File->file"."slug" AS "File.file.slug",
  "File->file"."topicId" AS "File.file.topicId",
  "File->file"."titleRender" AS "File.file.titleRender",
  "File->file"."titleSource" AS "File.file.titleSource",
  "File->file"."titleSourceLine" AS "File.file.titleSourceLine",
  "File->file"."render" AS "File.file.render",
  "File->file"."h1Render" AS "File.file.h1Render",
  "File->file"."h2Render" AS "File.file.h2Render",
  "File->file"."depth" AS "File.file.depth",
  "File->file"."score" AS "File.file.score",
  "File->file"."nestedSetIndex" AS "File.file.nestedSetIndex",
  "File->file"."nestedSetNextSibling" AS "File.file.nestedSetNextSibling",
  "File->file"."createdAt" AS "File.file.createdAt",
  "File->file"."updatedAt" AS "File.file.updatedAt",
  "File->file"."fileId" AS "File.file.fileId"
FROM
  (
    SELECT
      "Id"."id",
      "Id"."idid",
      "Id"."path",
      "Id"."toplevel_id",
      "Id"."ast_json",
      "Id"."macro_name",
      "Id"."createdAt",
      "Id"."updatedAt"
    FROM
      "Id" AS "Id"
    WHERE
      "Id"."idid" = '@barack-obama'
    LIMIT
      1
  ) AS "Id"
  LEFT OUTER JOIN "File" AS "File" ON "Id"."idid" = "File"."toplevel_id"
  LEFT OUTER JOIN "Article" AS "File->file" ON "File"."id" = "File->file"."fileId"

+227m
```
Hmmm, so no slow updates, only selects. Surprising!

<a id="_617"></a>
The first query is the:<a id="_618"></a>

```
const oldRef = await sequelize.models.Ref.findOne({
```

<a id="_619"></a>
OK, we manually reduced the first query to a subset:<a id="_620"></a>

```
SELECT
  "Ref"."to_id",
  "Ref"."from_id",
  "From"."idid" AS "From.idid",
  "From->File"."titleSource" AS "From->File.titleSource"
FROM "Ref"
INNER JOIN "Id" AS "From"
ON
  "Ref"."from_id" = "From"."idid" AND
  "Ref"."to_id" = '@barack-obama/test-data' AND
  "Ref"."type" = 0
INNER JOIN "File" AS "From->File"
  ON "From"."idid" = "From->File"."toplevel_id"
INNER JOIN "Article" AS "From->Article"
  ON "From->File"."id" = "From->Article"."fileId"
;
```
which we were certain should not be slow, and then by commenting things out learnt that foreign keys are not automatically indexed, so the `fileId` finding was super slow!!! OMG.

<a id="_621"></a>
That single one line change drops us down to half the creation time, amazing:<a id="_622"></a>

```
real    0m0.668s
user    0m0.638s
sys     0m0.035s
```

<a id="_623"></a>
On heroku, after manually doing:<a id="_624"></a>

```
create index article_file_id ON "Article" using btree ("fileId");
```
new article time fell down to 400ms, which is amazing. One liner! Special thanks to sequelize for the timing info.

<a id="_625"></a>
After this, the only DB activity that has more than 15ms is:<a id="_626"></a>

```
sequelize:sql:pg Executing (default): SELECT "id", "username", "ip", "displayName", "email", "image", "hash", "salt", "score", "followerCount", "admin", "verified", "verificationCode", "verificationCodeSent", "maxArticles", "maxArticleSize", "createdAt", "updatedAt" FROM "User" AS "User" WHERE "User"."username" = 'barack-obama'; +53ms
```
but we don't reproduce it in isolation, must be something else in play, e.g. something in parallel.

**Table of contents**

- [Article create and update slow on web update 1](article-create-and-update-slow-on-web-update-1.md)

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Progress spinner after submit](progress-spinner-after-submit.md)
