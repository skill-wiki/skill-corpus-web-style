# UppercaseSnakeForTrueConstants [rule] v0.1.0
Reserve `UPPER_SNAKE_CASE` for top-level program-wide constants whose value is fixed for the lifetime of the program and is also a primitive or deeply frozen value. Not every `const` deserves UPPER_SNAKE_CASE — only the ones that act as named magic values.
domain: web-style

## Checks
- [ ] The binding is at module scope (not a local `const` inside a function).
- [ ] The value is a primitive, a frozen object, or otherwise not meaningfully mutable.
- [ ] The name reads as a constant the consumer must not change: `MAX_RETRIES`, `DEFAULT_TIMEOUT_MS`, `API_BASE_URL`.
- [ ] Ordinary local `const` bindings stay in camelCase — `const user = await fetchUser()` is camelCase, not UPPER_SNAKE.

## Label
Use UPPER_SNAKE_CASE only for module-level deeply-immutable constants

## Label
Use UPPER_SNAKE_CASE only for module-level deeply-immutable constants
