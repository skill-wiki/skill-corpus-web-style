# OneBindingPerDeclaration [rule] v0.1.0
Write `const a = 1; const b = 2;` rather than `const a = 1, b = 2;`. One declaration per binding makes diffs cleaner, lets you initialise each from a different expression without contortions, and avoids the trap of accidentally giving every name in a comma-separated list the same `const`-vs-`let` modifier.
domain: web-style
