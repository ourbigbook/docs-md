# Publish to GitHub pages root page

↑ **Parent:** [`--publish-target github-pages`](publish-target-github-pages.md)

If you want to publish your root user page, which appears at `/` (e.g. [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io) for the user `cirosantilli`), GitHub annoyingly forces you to use the `master` branch for the HTML output:
- [https://github.com/isaacs/github/issues/212](https://github.com/isaacs/github/issues/212)
- [https://stackoverflow.com/questions/31439951/how-can-i-use-a-branch-other-than-master-for-user-github-pages](https://stackoverflow.com/questions/31439951/how-can-i-use-a-branch-other-than-master-for-user-github-pages)

This means that you must place your `.bigb` input files in a branch other than `master` to clear up `master` for the generated HTML.

`ourbigbook` automatically detects if your repository is a root repository or not by parsing `git remote` output, but you must setup the branches correctly yourself.

So on a new repository, you must [first checkout to a different branch](https://stackoverflow.com/questions/42871542/how-to-create-a-git-repository-with-the-default-branch-name-other-than-master) as in:
```
git init
git checkout -b dev
```
or to move an existing repository to a non-master branch:
```
git checkout -b dev
git push origin dev:dev
git branch -D master
git push --delete origin master
```

You then will also want to set your default repository branch to `dev` in the settings for that repository: [https://help.github.com/en/github/administering-a-repository/setting-the-default-branch](https://help.github.com/en/github/administering-a-repository/setting-the-default-branch)

## ↑ Ancestors (5)

1. [`--publish-target github-pages`](publish-target-github-pages.md)
2. [`--publish-target`](publish-target.md)
3. [OurBigBook CLI options](ourbigbook-cli-options.md)
4. [OurBigBook CLI](ourbigbook-cli.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Play with the template](play-with-the-template.md)
