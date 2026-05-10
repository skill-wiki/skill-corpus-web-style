# ImportForSideEffects [anti-pattern] v0.1.0
Writing `import './polyfills'` or `import 'register-handlers'` to trigger code execution at module load. The line has no value on the left of `from`, no symbols are bound, and the import is needed only because evaluating the file does work — registers a handler, patches a prototype, mutates a global.
domain: web-style
