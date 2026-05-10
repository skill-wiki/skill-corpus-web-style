# UseVar [anti-pattern] v0.1.0
Using `var` to declare any binding in modern JavaScript or TypeScript. `var` is hoisted to the enclosing function, has no temporal-dead-zone protection, and is silently re-declarable — three properties that exist only because `var` predates block scoping.
domain: web-style
