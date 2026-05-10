# @web-style — Airbnb + Google JavaScript style guides, atom-shaped

> 20 typed Prime atoms distilled from the Airbnb JavaScript Style Guide
> and the Google JavaScript Style Guide — naming, variable declarations,
> functions, objects/arrays, modules, plus core readability principles.

This is a **starter seed corpus** for the Skill Wiki marketplace. It gives an
AI coding agent an audited reference set covering the JavaScript style choices
that come up before any other code review can begin.

The corpus answers a common question: *"how do I write JavaScript that will pass
a senior reviewer's first read?"* The answer is no longer "skim two large
guides" — it is "load this Prime, follow the rules, avoid the anti-patterns."

---

## What's in the box

20 atoms across five categories.

| Category | Atoms | Kinds |
|---|---|---|
| Naming + variables | 8 | rule × 7, anti-pattern × 1 |
| Functions | 4 | rule × 3, anti-pattern × 1 |
| Objects + arrays | 3 | rule × 3 |
| Modules | 3 | rule × 1, anti-pattern × 2 |
| Principles | 2 | principle × 2 |
| **Total** | **20** | — |

Each `.prime` file carries a `// Source:` header pointing to the exact section
of the Airbnb or Google guide it summarises.

---

## Install

```bash
prime install @web-style
```

The marketplace entry will be live once `skill-wiki/website`'s
`data/skills.yaml` is updated to register `@web-style`.

### As an MCP server in Claude Code

```json
{
  "mcpServers": {
    "web-style": {
      "command": "bunx",
      "args": ["@skill-wiki/mcp-server-core"],
      "env": {
        "PRIME_DIR": "/abs/path/to/skill-corpus-web-style/compiled"
      }
    }
  }
}
```

The agent now sees a 20-atom JS-style index on every turn. It pulls the
relevant atoms when the task touches a style concern (naming, declarations,
modules) and ignores them otherwise.

---

## License

This Prime is dual-licensed:

| Layer | License |
|---|---|
| **Code** (pack.yaml, domain.yaml, build glue, packaging) | Apache-2.0 |
| **Atom content** — Airbnb-derived | MIT (Airbnb) |
| **Atom content** — Google-derived | CC-BY 3.0 (Google) |

Each `.prime` file links the specific guide section it summarises and carries
its own attribution header. See `LICENSE` for full text and the third-party
attribution block.

If you adapt or extend the corpus:

1. Keep the per-file `// Source: …` attribution headers.
2. Honour MIT and CC-BY 3.0 attribution requirements forward into derivatives.
3. Note your changes near the original attribution.

---

## How to compile

The corpus is checked-in pre-compiled (`compiled/_index.xml` + per-atom
directories). To rebuild from sources:

```bash
# from the repo root
bun ../prime-system/scripts/build-atom-dirs.ts \
  --src primes/sources \
  --out compiled

# Expected output:
# Found 20 .prime files in primes/sources
# ... per-atom emit lines ...
# 20 atoms compiled
#   → compiled/_index.xml (~2.0k tokens, 20 atoms)
```

The build script lives in the
[`prime-system`](https://github.com/skill-wiki/prime-system) repo. Clone both
side-by-side, or vendor the script in if you prefer.

---

## Reading order

1. **`principle-clarity-over-cleverness`** + **`principle-consistency-within-codebase`** —
   the two heuristics every other rule cashes out from.
2. The **rule + anti-pattern** pairs in declarations, functions, and modules —
   that pair is the operational core for that scope.
3. The naming rules (`camelCase`, `PascalCase`, `UPPER_SNAKE`, descriptive) —
   the smallest set that makes a codebase legible.

---

## Contributing

This is a seed set. The full Airbnb + Google guides cover hundreds of decisions;
we picked 20 because that is the smallest set that demonstrates the model and is
useful by itself.

Good additions:

- **Control flow** — early returns, ternary depth, `switch` cases.
- **Comments** — JSDoc style, when comments are required, when they are wrong.
- **Whitespace** — end-of-line semicolons, brace style, indent width.
- **Type hints** — TypeScript-specific style notes (Google's TS guide is a
  separate corpus candidate).
- **React-specific atoms** — JSX boolean props, hook ordering, `key` prop rules.

Open a PR. Keep:

- Atoms terse — atom-shaped, not paraphrased prose.
- One `.prime` file per atom.
- The `// Source: …` header pointing to the originating guide section.
- Edges (`requires` / `enhances` / `contradicts` / `related`) where the
  relationship is real, not for decoration.
- A passing `bun ../prime-system/scripts/build-atom-dirs.ts ...` run.

---

## Provenance

- **Knowledge sources:**
  - Airbnb JavaScript Style Guide, MIT, https://github.com/airbnb/javascript
  - Google JavaScript Style Guide, CC-BY 3.0, https://google.github.io/styleguide/jsguide.html
- **Atom packaging:** Skill Wiki contributors, Apache-2.0
- **Distillation:** the prose in each atom is heavily compressed and
  re-shaped from the originals; this is fair use within the source licenses,
  but the substance is Airbnb's and Google's work.
