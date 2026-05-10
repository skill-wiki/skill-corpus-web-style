# PreferConstOverLet [rule] v0.1.0
Declare every binding with `const` by default. Reach for `let` only when the binding is genuinely reassigned. A `const` binding signals to the reader that the slot will not change — that signal is a load-bearing part of readability.
domain: web-style
