# PreferFunctionalArrayMethods [rule] v0.1.0
When iterating an array to produce a derived value — a new array, a single accumulator, the first match, a boolean — use the corresponding higher-order method. The named method tells the reader what the loop is *for* in one word; a `for` loop with a hand-rolled accumulator buries that intent under index plumbing.
domain: web-style

## Checks
- [ ] Mapping uses `array.map(fn)`, not a `for` loop pushing into a fresh array.
- [ ] Filtering uses `array.filter(predicate)`.
- [ ] Aggregating to a scalar uses `array.reduce(reducer, init)`.
- [ ] Membership / first-match uses `array.some` / `array.find`; existence uses `array.includes`.
- [ ] ESLint `no-iterator` (forbid `iterator`/`__iterator__`) is enabled; teams may add `no-restricted-syntax` to flag plain `for` over arrays.

## Label
Use `map` / `filter` / `reduce` / `find` over hand-rolled `for` loops over arrays
