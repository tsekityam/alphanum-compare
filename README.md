# alphanum-compare

[![npm version](https://badge.fury.io/js/alphanum-compare.svg)](https://badge.fury.io/js/alphanum-compare)
[![Node.js CI](https://github.com/tsekityam/alphanum-compare/actions/workflows/test.yml/badge.svg)](https://github.com/tsekityam/alphanum-compare/actions/workflows/test.yml)
[![codecov](https://codecov.io/gh/tsekityam/alphanum-compare/branch/main/graph/badge.svg?token=DHFqZcVnZR)](https://codecov.io/gh/tsekityam/alphanum-compare)
[![Known Vulnerabilities](https://snyk.io/test/github/tsekityam/alphanum-compare/badge.svg)](https://snyk.io/test/github/tsekityam/alphanum-compare)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Ftsekityam%2Falphanum-compare.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Ftsekityam%2Falphanum-compare?ref=badge_shield)

Compare function extrated from [alphanum-sort](https://github.com/trysound/alphanum-sort). It can be used as `compareFunction` in `Array.prototype.sort()`.

## Install

`npm install alphanum-compare`

## Usage

```ts
import compareFn from "alphanum-compare";

console.log("5".localeCompare("10")); // 1, NO GOOD
console.log(compareFn("5", "10")); // -1, GOOD

console.log(compareFn("-5", "5")); // 1, NO GOOD
console.log(compareFn("-5", "5", { sign: true })); // -1, GOOD

console.log(["item20", "item19", "item1", "item10", "item2"].sort(compareFn));
// ['item1', 'item2', 'item10', 'item19', 'item20']
```

[CodeSandbox](https://codesandbox.io/s/alphanum-compare-demo-bfhln)

### `compareFn(a: number | string, b: number | string, opts?: Options): number`

It returns a negative value if first argument is less than second argument, zero if they're equal and a positive value otherwise.

#### Options

- `insensitive?: boolean`

  Compares items case insensitively. _(Default: `false`)_

- `sign?: boolean`

  Allows `+` and `-` characters before numbers. _(Default: `false`)_

## License

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Ftsekityam%2Falphanum-compare.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Ftsekityam%2Falphanum-compare?ref=badge_large)
