# PascalCaseClassesAndTypes [rule] v0.1.0
Names for things that produce instances or describe shapes — classes, constructor functions, TypeScript types, interfaces, and enum names — are written in `PascalCase`: every word capitalised including the first.
domain: web-style

## Checks
- [ ] Class declarations match `[A-Z][a-zA-Z0-9]*` (e.g. `UserSession`, `HttpClient`).
- [ ] TypeScript `type`, `interface`, and `enum` declarations use the same PascalCase shape.
- [ ] React component identifiers — function or class — are PascalCase; lowercase names are reserved for HTML intrinsics.
- [ ] ESLint `new-cap` rule (or TypeScript naming-convention) enforces this.

## Label
Classes, constructors, type aliases, interfaces, and enums use PascalCase
