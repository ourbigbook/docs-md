# Run an isolated OurBigBook master

↑ **Parent:** [Run OurBigBook master](run-ourbigbook-master.md)

[Run OurBigBook master](run-ourbigbook-master.md) mentions how to install and then run OurBigBook master globally, which is useful build some projects locally on master.

To instead install locally in the current directory only instead, which can be useful for bisection:
```
npm install
ln -s .. node_modules/ourbigbook
npm run build-assets
```

You can now run tests as:
```
npm test
```
or the executable interactively as:
```
./ourbigbook .
```
It also works from a subdirectory:
```
mkdir -p tmp
cd tmp
../ourbigbook .
```

## ↑ Ancestors (3)

1. [Run OurBigBook master](run-ourbigbook-master.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)
