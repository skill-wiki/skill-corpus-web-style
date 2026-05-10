# CamelCaseVariablesAndFunctions [rule] v0.1.0
Local variables, parameters, function names, methods, and non-static class fields are written in `camelCase` — first word lowercase, every subsequent word capitalised, no underscores or hyphens. Both Airbnb and Google's style guides require this.
domain: web-style

## Checks
- [ ] Names match the regex `[a-z][a-zA-Z0-9]*` for ordinary identifiers.
- [ ] No leading or trailing underscores on public names; no `snake_case` for ordinary identifiers.
- [ ] Acronyms in names are treated as words: `parseHtmlUrl`, not `parseHTMLURL`.
- [ ] ESLint `camelcase` rule is enabled.

## Label
Use camelCase for variables, functions, methods, and instance properties
