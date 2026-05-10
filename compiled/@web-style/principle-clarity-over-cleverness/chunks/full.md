# ClarityOverCleverness [principle] v0.1.0
Code is read many more times than it is written. Optimise for the next reader — usually a tired version of yourself in six months — rather than for a reduction in keystrokes today. Where the language offers a terse form and an explicit form that mean the same thing, pick the explicit one unless the terse form is itself a well-known idiom.
> When a clever idiom and an obvious idiom both work, pick the obvious one. Save the cleverness for the cases where it earns its keep — performance hot paths backed by benchmarks, language-level constraints that allow no other expression. Everywhere else, write the boring version that the next reader can scan in one pass.
domain: web-style

## Applies To
- Naming — full descriptive words over hand-rolled abbreviations.
- Control flow — early returns and named helpers over deeply nested ternaries.
- Data shaping — destructuring, named returns, and explicit object literals over positional tuples.
- Imports — named imports of specific symbols over wildcard or side-effect imports.
