# `lib:` vs `cli:` tests

↑ **Parent:** [Test system](test-system.md)

There are two types of test in our test suite:
- tests that call the `ourbigbook.convert` [JavaScript API](ourbigbook-library.md) directly.  
  These tests are prefixed with `lib: `

  These tests don't actually create files in the filesystem, and just mock the filesystem instead with a dictionary.

  Database access is not mocked however, we just use Sqlite's fantastic in-memory mode.

  Whenever possible, these tests check their results just from the [abstract syntax tree](abstract-syntax-tree.md) tree returned by the API, which is cleaner than parsing the HTML. But sometimes HTML parsing is inevitable.
- tests that call the [`ourbigbook` executable](ourbigbook-cli.md) itself:
  - their titles are prefixed with `cli: `
  - they tend to be a lot slower than the API test
  - can test functionality that is done outside of the `ourbigbook.convert` JavaScript API, notably stuff prevent in ourbigbook, so they are more end to end
  - don't do any mocking, and could therefore be more representative.

    However, as of 2022, we have basically eliminated all the hard database access mocking and are using the main database methods directly.

    So all that has to be mocked is basically stuff done in the ourbigbook executable itself.

    This means that except for more specific options, the key functionality of ourbigbook, which is to convert multiple paths, can be done very well in a non executable test.

    The only major difference is that instead of passing command line arguments like in `ourbigbook .` to convert multiple files in a directory, you have to use `convert_before` and `convert_before_norender` and specify conversion order one by one.

    This test robustness is new as of 2022, and many tests were previously written with executable that would now also work as unit tests, and we generally want that to be the case to make the tests go faster.
  - work by creating an actual physical filesystem under `_out/test/<normalized-test-title>` with the OurBigBook files and other files like `ourbigbook.json`, and then running the executable on that directory.

    `npm test` first deletes the `_out/test` directory before running the tests. After running, the generated files are kept so you can inspect them to help debug any issues.
  - all these tests check their results by parsing the HTML and searching for elements, since here we don't have access to the [abstract syntax tree](abstract-syntax-tree.md). It wouldn't be impossible to obtain it however, as it is likely already JSON serializable.

## ↑ Ancestors (3)

1. [Test system](test-system.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)
