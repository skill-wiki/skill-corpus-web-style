# ObjectShorthandAndComputedKeys [rule] v0.1.0
Build objects with the most expressive ES2015+ syntax available at the literal: shorthand for properties whose key matches the source variable, method shorthand for inline methods, and computed-key syntax (`{ [expr]: value }`) for keys derived at construction time. Each form replaces a more verbose pre-ES2015 idiom and signals intent clearly.
domain: web-style

## Checks
- [ ] `const user = { id, name }` rather than `{ id: id, name: name }` when the variable name matches.
- [ ] Methods on object literals use shorthand: `{ greet() { … } }`, not `{ greet: function () { … } }`.
- [ ] Dynamic keys are placed in the literal with `[…]` rather than created and assigned in a follow-up statement.
- [ ] Group shorthand properties at the start of the literal, before longhand properties — Airbnb's grouping rule.

## Label
Use property shorthand, method shorthand, and computed keys at the literal

## Label
Use property shorthand, method shorthand, and computed keys at the literal
