# UppercaseSnakeForTrueConstants [rule] v0.1.0
Reserve `UPPER_SNAKE_CASE` for top-level program-wide constants whose value is fixed for the lifetime of the program and is also a primitive or deeply frozen value. Not every `const` deserves UPPER_SNAKE_CASE — only the ones that act as named magic values.
domain: web-style
