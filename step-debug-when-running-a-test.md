# Step debug when running a test

↑ **Parent:** [Test system](test-system.md)

Step debug during a test run. Add the statement:
```
debugger;
```
to where you want to break in the code, and then run:
```
npm run testi -- -g 'p with id before'
```
where `i` in `testi` stands for `inspect` from `node inspect`. Also consider the alias:
```
npmtgi() ( npm run testi -- -g "$*" )
```

Note however that this does not work for tests that run the `ourbigbook` executable itself, since those spawn a separate process. TODO how to do it? Tried along:
```
const out = child_process.spawnSync('node', ['inspect', 'ourbigbook'].concat(options.args), {
  cwd: tmpdir,
  input: options.stdin,
  stdio: 'inherit',
});
```
but not working, related: [https://stackoverflow.com/questions/23612087/gulp-target-to-debug-mocha-tests](https://stackoverflow.com/questions/23612087/gulp-target-to-debug-mocha-tests) So for now, we are just printing the command being run as in:
```
cmd: cd _out/test/executable-ourbigbook.json-outputOutOfTree && ourbigbook --split-headers .
```
so you can just re-run it manually with `node inspect` as in:
```
cd _out/test/executable-ourbigbook.json-outputoutoftree && node inspect "../../../ourbigbook" --split-headers .
```
This works since the `tmp` directory is not deleted in case of failure.

## ↑ Ancestors (3)

1. [Test system](test-system.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)
