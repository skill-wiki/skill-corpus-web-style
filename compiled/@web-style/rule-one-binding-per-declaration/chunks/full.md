# OneBindingPerDeclaration [rule] v0.1.0
Write `const a = 1; const b = 2;` rather than `const a = 1, b = 2;`. One declaration per binding makes diffs cleaner, lets you initialise each from a different expression without contortions, and avoids the trap of accidentally giving every name in a comma-separated list the same `const`-vs-`let` modifier.
domain: web-style

## Checks
- [ ] No `const a = 1, b = 2` patterns — each binding is its own statement.
- [ ] ESLint `one-var` rule set to `["error", "never"]` (or equivalent).
- [ ] Destructuring counts as one binding for this rule: `const { a, b } = obj` is fine, since the source is a single expression.

## Label
Declare one binding per `const` or `let` statement

## Label
Declare one binding per `const` or `let` statement
