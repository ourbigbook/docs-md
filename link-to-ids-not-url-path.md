# Link to IDs, not URL path

↑ **Parent:** [Cross file internal link](cross-file-internal-link.md)

This section describes the philosophy of [internal links](internal-link.md).

In many static website generators, you just link to URL specific paths of internal headers.

In OurBigBook, [internal links](internal-link.md) point to IDs, not paths.

For example, suppose "Superconductivity" is a descendant of "Condensed Matter Physics", and that the source for both is located at `condensed-matter-physics.bigb`, so that both appear on the same .html page `condensed-matter-physics.html`.

When linking to Superconductivity from an external page such as `statistical-physics.bigb` you write just `<superconductivity>` and NOT `<condensed-matter-physics#superconductivity>`. OurBigBook then automatically trakcs where superconductivity is located and produces `href="condensed-matter-physics#superconductivity"` for you.

This is important because on a static website, the location of headers might change. E.g. if you start writing a lot about superconductivity you would eventually want to split it to its own page, `superconductivity.html` otherwise page loads for `condensed-matter-physics.html` would become too slow as that file would become too large.

But if your links read `<condensed-matter-physics#superconductivity>`, and all links would break when you move things around.

So instead, you simply link to the ID `<superconductivity>`, and ourbigbook renders links correctly for you wherever the output lands.

When moving headers to separate pages, it is true that existing links to subheaders will break, but that simply cannot be helped. Large pages must be split into smaller ones. The issue can be mitigated in the following ways:
- [`-S`, `--split-headers`](split-headers.md), which readers will eventually understand are better permalinks
- [JavaScript redirect to split on missing ID](javascript-redirect-to-split-on-missing-id.md), which automatically redirect `condensed-matter-physics#superconductivity` to `superconductivity`, potentially hitting a [split header](split-headers.md) if the current page does not contain the HTML ID `superconductivity`.

For [OurBigBook Web](ourbigbook-web.md), this is even more important, as we have [dynamic article trees](ourbigbook-web-dynamic-article-tree.md), so every header can appear on top.

If you really want to to use scopes, e.g. enforce the ID of "superconductivity" to be "condensed-matter-physics/superconductivity", then you can use the [scope](h-scope-argument.md) feature. However, this particular case would likely be a bad use case for that feature. You want your IDs to be as short as possible, which causes less need for refactoring, and makes [topics](ourbigbook-web-topics.md) on [OurBigBook Web](ourbigbook-web.md) more likely to have matches from other users.

<a id="image-cross-file-internal-link-link-to-ids-not-url-path"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/x/hilbert-space-arrow.png" alt="" height="571">

**[Figure 45](#image-cross-file-internal-link-link-to-ids-not-url-path). Cross file internal link**.

## ↑ Ancestors (5)

1. [Cross file internal link](cross-file-internal-link.md)
2. [Internal link](internal-link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
