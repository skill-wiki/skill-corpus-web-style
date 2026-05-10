# ImportForSideEffects [anti-pattern] v0.1.0
Writing `import './polyfills'` or `import 'register-handlers'` to trigger code execution at module load. The line has no value on the left of `from`, no symbols are bound, and the import is needed only because evaluating the file does work — registers a handler, patches a prototype, mutates a global.
domain: web-style

## Label
Importing a module purely for its side effects

## Why Bad
Side-effect imports break tree-shaking: bundlers cannot drop the module even if nothing else references it, because they cannot prove the module is pure. Order of evaluation suddenly matters and is hard to see — one teammate moves the import, polyfills load after the code that needs them, the bug is reproducible only in production. The dependency graph also becomes invisible: nothing in the importing file says "this module set up timers / event listeners / globals".

## Instead Do
```
    Export an explicit initialiser and call it from the module's
    composition root:

      // polyfills.ts
      export function installPolyfills() { … }

      // entry.ts
      import { installPolyfills } from './polyfills';
      installPolyfills();

    Now the side effect is visible at the call site, the order is fixed
    by code rather than by import order, and tree-shaking sees a
    referenced symbol it can keep or drop based on usage.
  
```
