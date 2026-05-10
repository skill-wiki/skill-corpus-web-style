# ArrowFunctionsForCallbacks [rule] v0.1.0
When the function is anonymous and passed inline as an argument or assigned to a binding, use an arrow function. Arrow functions inherit `this` from the enclosing scope, are terser, and signal "this is not a method, just a value-returning expression" at the call site.
domain: web-style

## Checks
- [ ] `array.map((x) => x.id)` rather than `array.map(function (x) { return x.id })`.
- [ ] Single-expression arrow bodies omit braces and `return`: `(x) => x.id`, not `(x) => { return x.id }`.
- [ ] Use parentheses around the parameter list whenever there are zero, two-or-more, or destructured parameters; many teams require parens always for consistency (Airbnb does).
- [ ] ESLint `prefer-arrow-callback` and `arrow-body-style` are configured.

## Label
Use arrow functions for anonymous callbacks
