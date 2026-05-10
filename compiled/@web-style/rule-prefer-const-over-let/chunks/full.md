# PreferConstOverLet [rule] v0.1.0
Declare every binding with `const` by default. Reach for `let` only when the binding is genuinely reassigned. A `const` binding signals to the reader that the slot will not change — that signal is a load-bearing part of readability.
domain: web-style

## Checks
- [ ] Every variable that is not reassigned in its scope is declared with `const`.
- [ ] `let` appears only on bindings that have at least one assignment after the declaration.
- [ ] Loop counters and accumulators that genuinely change use `let`; everything else is `const`.
- [ ] ESLint `prefer-const` is on as `error` and `no-const-assign` is on as `error`.

## Label
Use `const` for all references; only fall back to `let` when reassignment is required

## Label
Use `const` for all references; only fall back to `let` when reassignment is required
