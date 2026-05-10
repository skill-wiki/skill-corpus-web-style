# NamedImportsStablePaths [rule] v0.1.0
Use `import { foo, bar } from './lib'` rather than `import lib from './lib'` followed by `lib.foo` and `lib.bar`. Named imports document the API surface, make tree-shaking effective, and resist the trap of a default export later being replaced by a namespace object.
domain: web-style

## Checks
- [ ] Each external value used in the file is imported by name at the top.
- [ ] Default imports appear only when the source module has exactly one logical export (e.g. a React component file).
- [ ] Import paths are stable: prefer package roots (`'lodash/get'`, `'@scope/pkg'`) over cross-package deep paths into `dist/` or `src/`.
- [ ] Imports are sorted: external packages first, then internal, then relative — and grouped with blank lines (Airbnb / ESLint `import/order`).

## Label
Prefer named imports from stable paths; reserve default imports for true single-export modules
