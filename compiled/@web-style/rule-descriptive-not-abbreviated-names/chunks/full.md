# DescriptiveNotAbbreviatedNames [rule] v0.1.0
Identifier length follows information content. Use whole words that describe the role of the binding. Reserve single-letter names for canonical mathematical loop indices (`i`, `j`) or for ubiquitous higher-order callbacks (`(x) => x.id`). Avoid hand-rolled abbreviations — they save typing once and cost reading every time after.
domain: web-style

## Checks
- [ ] No single-letter names except canonical loop indices and tiny lambdas.
- [ ] Avoid hand-rolled abbreviations (`usrLst`, `qryRslt`, `cb`, `fn`); spell `userList`, `queryResult`, `callback`, `function`.
- [ ] Use only abbreviations the entire industry already shares (`url`, `id`, `db`, `ms`, `xml`, `json`, `http`).
- [ ] Boolean names are predicates: `isActive`, `hasPermission`, `canEdit`, `shouldRetry` — not `active`, `permission`, `edit`, `retry`.

## Label
Names describe intent in full words; do not abbreviate beyond convention

## Label
Names describe intent in full words; do not abbreviate beyond convention
