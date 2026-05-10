# PreferSpreadOverApply [rule] v0.1.0
When passing a list of values as positional arguments, spread the array (`fn(...args)`) instead of calling `fn.apply(null, args)`. When collecting variadic arguments, use rest parameters (`function fn(...args)`) instead of inspecting the legacy `arguments` object. Both spread and rest are dedicated syntax for the job, and both compose cleanly with arrow functions.
domain: web-style
