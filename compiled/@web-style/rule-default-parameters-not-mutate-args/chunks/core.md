# DefaultParametersNotMutateArgs [rule] v0.1.0
Express defaults in the parameter list with `=`. Do not patch missing values inside the body with reassignment, `||`, or by writing into `arguments`. Default-parameter syntax keeps the function signature self-documenting and makes the default value visible at the call boundary.
domain: web-style

## Checks
- [ ] Defaults are written `function fn(x = 0, y = []) { … }`, not `if (x === undefined) x = 0`.
- [ ] No reads of or writes to the `arguments` object — use rest parameters instead: `function fn(...args)`.
- [ ] Default-valued parameters come last in the signature so callers can omit them positionally.
- [ ] Default expressions are not side-effectful; they evaluate per call.

## Label
Use ES6 default parameters; never mutate the arguments object
