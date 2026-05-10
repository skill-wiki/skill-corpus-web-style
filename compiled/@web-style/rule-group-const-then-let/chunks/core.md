# GroupConstThenLet [rule] v0.1.0
Within a scope, list every `const` binding before any `let` binding. The reader can then scan the top of the scope and immediately see which bindings are fixed and which will mutate, without re-checking each line.
domain: web-style

## Checks
- [ ] All `const` declarations appear above the first `let` in the same scope.
- [ ] Imports and other top-of-file boilerplate sit above this group.
- [ ] Reordering a `const` to fit this rule does not change its initialisation order — declare the dependency `const` before the `const` that needs it.

## Label
Group all `const` declarations first, then group all `let` declarations
