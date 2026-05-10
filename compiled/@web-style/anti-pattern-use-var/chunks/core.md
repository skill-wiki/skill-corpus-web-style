# UseVar [anti-pattern] v0.1.0
Using `var` to declare any binding in modern JavaScript or TypeScript. `var` is hoisted to the enclosing function, has no temporal-dead-zone protection, and is silently re-declarable — three properties that exist only because `var` predates block scoping.
domain: web-style

## Label
Declaring variables with `var`

## Why Bad
`var` leaks across blocks. A `var i` inside an `if` is visible at the top of the function and after the block exits. Re-declaring the same `var` is silent. Hoisting means the binding exists before its declaration line, which surprises readers and breaks closures inside loops. Every modern style guide and lint configuration treats `var` as legacy noise.

## Instead Do
```
    Use `const` for bindings you do not reassign and `let` for bindings
    you do. Both are block-scoped, neither is hoisted past the start of
    the block, and both throw on duplicate declaration. Turn on the
    ESLint `no-var` rule as `error` to catch regressions.
  
```
