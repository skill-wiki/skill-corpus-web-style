# MutableNamedExport [anti-pattern] v0.1.0
Declaring `export let counter = 0` (or similar) and then reassigning it elsewhere in the module so importers' references update with each change. Ditto exporting an object whose properties are reassigned post-import as a way to push state across module boundaries.
domain: web-style
