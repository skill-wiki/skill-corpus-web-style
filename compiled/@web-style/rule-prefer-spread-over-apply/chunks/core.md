# PreferSpreadOverApply [rule] v0.1.0
When passing a list of values as positional arguments, spread the array (`fn(...args)`) instead of calling `fn.apply(null, args)`. When collecting variadic arguments, use rest parameters (`function fn(...args)`) instead of inspecting the legacy `arguments` object. Both spread and rest are dedicated syntax for the job, and both compose cleanly with arrow functions.
domain: web-style

## Checks
- [ ] Variadic forwarding is `wrapper(...args)`, not `wrapper.apply(this, args)`.
- [ ] Variadic capture is `function fn(...args) { … }`, not `function fn() { var args = arguments; … }`.
- [ ] Array copy is `[...source]` or `Array.from(source)`, not `source.slice()` followed by mutation patterns.
- [ ] Object copy / merge is `{ ...source, override }`, not `Object.assign({}, source, { override })` (both work; spread is the style choice).

## Label
Prefer the spread operator over `.apply()` and `arguments`-based variadic plumbing
