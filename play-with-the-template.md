# Play with the template

↑ **Parent:** [OurBigBook CLI quick start](ourbigbook-cli-quick-start.md)

Learn the syntax basics in 5 minutes: [https://docs.ourbigbook.com/_obb/dist/editor](https://docs.ourbigbook.com/_obb/dist/editor).

First ensure that Node.js is installed in your computer. You should be able to successfully the following command successfully from a terminal:
```
node --version
```

Now let's play with [an OurBigBook template](https://github.com/ourbigbook/template) locally:
```
git clone https://github.com/ourbigbook/template
cd template
npm install
npx ourbigbook .
firefox _out/html/index.html
```
That template can be seen rendered live at: [http://cirosantilli.com/ourbigbook-generate-multifile/](http://cirosantilli.com/ourbigbook-generate-multifile/) Other templates are documented at: [`--generate`](generate.md).

To [publish to GitHub Pages](publish-target-github-pages.md) on your repository you can just fork the repository [https://github.com/ourbigbook/template](https://github.com/ourbigbook/template) to your own [https://github.com/johndoe/template](https://github.com/johndoe/template) and then:
```
git remote set-url origin git@github.com:johndoe/template.git
npx ourbigbook --publish
```
and it should now be visible at: [https://johndoe.github.io/template](https://johndoe.github.io/template)

Then, every time you make a change you can publish the new version with:
```
git add .
git commit --message 'hacked stuff'
ourbigbook --publish .
```
or equivalently with the [`-P, --publish-commit <commit-message>`](publish-commit.md) shortcut:
```
ourbigbook --publish-commit 'hacked stuff'
```

If you want to publish to your root page [https://johndoe.github.io](https://johndoe.github.io) instead of [https://johndoe.github.io/template](https://johndoe.github.io/template) you need to rename the `master` branch to `dev` as mentioned at [publish to GitHub pages root page](publish-to-github-pages-root-page.md):
```
git remote set-url origin git@github.com:johndoe/johndoe.github.io.git

# Rename master to dev, and delete the old master.
git checkout -b dev
git push origin dev:dev
git branch -D master
git push --delete origin master

npx ourbigbook --publish
```

The following files of the template control the global style of the output, and you are free to edit them:
- `ourbigbook.liquid.html`: global HTML template in [Liquid format](https://shopify.github.io/liquid/). Available variables are documented at [Section "`--template`"](template.md)
- `main.scss`: [Sass](https://sass-lang.com/) file that gets converted to raw CSS `main.css` by `npx ourbigbook .`.

  Sass is just much more convenient to write than raw CSS.

  That file gets included into the global HTML template inside `ourbigbook.liquid.html` at:
  ```
  <link rel="stylesheet" href="{{ root_relpath }}main.css">
  ```

## ↑ Ancestors (3)

1. [OurBigBook CLI quick start](ourbigbook-cli-quick-start.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (5)

- [Features](features.md)
- [Out-of-box testing](out-of-box-testing.md)
- [`--publish-target github-pages`](publish-target-github-pages.md)
- [Useless knowledge](useless-knowledge.md)
- [Visual Studio Code quick start](visual-studio-code-quick-start.md)
