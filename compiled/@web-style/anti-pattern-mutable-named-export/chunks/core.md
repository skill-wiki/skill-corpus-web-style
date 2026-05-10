# MutableNamedExport [anti-pattern] v0.1.0
Declaring `export let counter = 0` (or similar) and then reassigning it elsewhere in the module so importers' references update with each change. Ditto exporting an object whose properties are reassigned post-import as a way to push state across module boundaries.
domain: web-style

## Label
Exporting a `let` binding and mutating it after the module loads

## Why Bad
Module-level mutable state is a hidden global. Importers cannot tell from the import line that the value will change under them; they often capture a stale reference into a local and miss the updates anyway. Build tooling (rollup, esbuild, modern bundlers) optimises imports under the assumption that named exports are read-once at module load — mutating them defeats those optimisations and can crash live-bindings semantics across bundlers.

## Instead Do
```
    Export a function that returns the current value, or export a class /
    object whose methods provide controlled access. If the module truly
    represents shared mutable state, make that explicit:

      let value = 0;
      export const getValue = () => value;
      export const setValue = (next) => { value = next; };

    Now every read goes through a function call, which is honest about
    the binding being live, and importers cannot accidentally cache it.
  
```
