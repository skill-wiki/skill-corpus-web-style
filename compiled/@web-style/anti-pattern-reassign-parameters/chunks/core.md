# ReassignParameters [anti-pattern] v0.1.0
Treating a parameter as a mutable local — assigning to it, mutating its properties when the caller did not opt in, or using it as scratch space. The parameter binding is part of the function's contract with its callers; rewriting it in the body breaks the obvious mapping between the call site and what runs.
domain: web-style

## Label
Reassigning a function parameter inside the function body

## Why Bad
When a parameter is reassigned, every reference to that name inside the function may mean the original argument or the rewritten value depending on where you are reading. Debuggers, stack traces, and grep all become misleading. Mutating an object parameter without the caller asking for that mutation creates spooky action-at-a-distance: the caller's value changes after the call returns.

## Instead Do
```
    Introduce a new local binding instead. If you need a sanitised
    version of `user`, write `const sanitised = canonicalise(user)` and
    use `sanitised` in the rest of the body. If you need to return a
    modified copy, return it; do not write into the caller's object.

    Configure ESLint `no-param-reassign` as `error` with
    `props: true` to catch nested mutations as well.
  
```
