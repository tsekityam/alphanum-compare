# alphanum-compare

Compare function extrated from [alphanum-sort](https://github.com/trysound/alphanum-sort). It can be used as `compareFunction` in `Array.prototype.sort()`.

## Install

`yarn add alphanum-compare`

## Usage

```ts
import compareFn from "alphanum-compare";

const result = ["item20", "item19", "item1", "item10", "item2"].sort(compareFn);
// ['item1', 'item2', 'item10', 'item19', 'item20']
```

### `compareFn(a: string, b: string, opts?: { sign?: boolean }): number`

It returns a negative value if first argument is less than second argument, zero if they're equal and a positive value otherwise.

#### Options

- `sign?: boolean`: Allows `+` and `-` characters before numbers. _(Default: `false`)_
