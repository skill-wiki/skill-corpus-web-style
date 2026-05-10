# GroupConstThenLet [rule] v0.1.0
Within a scope, list every `const` binding before any `let` binding. The reader can then scan the top of the scope and immediately see which bindings are fixed and which will mutate, without re-checking each line.
domain: web-style
