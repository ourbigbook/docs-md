# Out-of-box testing

↑ **Parent:** [Release procedure](release-procedure.md)

After publishing, a good minimal sanity check is to ensure that you can render the template as mentioned in [play with the template](play-with-the-template.md):
```
cd ~
# Get rid of the global npm link development version just to make sure it is not being used.
npm uninstall -g ourbigbook
git clone https://github.com/ourbigbook/template
cd template
npm install
npx ourbigbook .
firefox _out/html/index.html
```

## ↑ Ancestors (3)

1. [Release procedure](release-procedure.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)
