# Build the docs

↑ **Parent:** [Developing OurBigBook](developing-ourbigbook.md)

After following [Run OurBigBook master](run-ourbigbook-master.md), clone the [OurBigBook media repository](ourbigbook-media-repository.md) alongside this repository to build the docs. From the `ourbigbook` directory:
```
git clone https://github.com/ourbigbook/ourbigbook-media ../ourbigbook-media
ourbigbook .
```
This fetches the required media such as images used by the HTML. This way you can build and see the entire website locally.

We don't track this as a submodule for the following reasons:
- Heroku would automatically clone it on deployment. There's no clean way to avoid this currently: [https://stackoverflow.com/questions/38996105/can-heroku-ignore-git-submodules-on-deploy](https://stackoverflow.com/questions/38996105/can-heroku-ignore-git-submodules-on-deploy)
- the media repository may get so big that force pushes or removal from GitHub to another form of storage could become necessary, which would break submodule behaviour

## ↑ Ancestors (2)

1. [Developing OurBigBook](developing-ourbigbook.md)
2. [OurBigBook Project](split.md)
