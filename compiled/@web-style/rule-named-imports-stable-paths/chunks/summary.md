# NamedImportsStablePaths [rule] v0.1.0
Use `import { foo, bar } from './lib'` rather than `import lib from './lib'` followed by `lib.foo` and `lib.bar`. Named imports document the API surface, make tree-shaking effective, and resist the trap of a default export later being replaced by a namespace object.
domain: web-style
