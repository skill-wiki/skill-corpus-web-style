# DestructureObjectsAndArrays [rule] v0.1.0
When a function reads more than one property of an object — its parameter, its return value, or any local — pull them out with destructuring. When a function returns several named values, return an object and let the caller destructure; do not return an array unless the order is meaningful and stable forever.
domain: web-style

## Checks
- [ ] Multi-property reads use `const { a, b } = source` rather than repeated `source.a`, `source.b`.
- [ ] Function parameters that are options bags are destructured in the signature: `function fn({ id, name }) { … }`.
- [ ] Multi-value returns are objects, not positional arrays — except for canonical ordered pairs (e.g. React's `useState`).
- [ ] Defaults inside destructuring are written `const { a = 0, b = '' } = source`.

## Label
Destructure when accessing multiple properties; prefer object destructuring for multi-value returns
