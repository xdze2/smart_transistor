# Wiki Schema

Conventions for the `knowledge_base/` directory. Minimal for now — will evolve.

## File structure

```
knowledge_base/
├── WIKI_SCHEMA.md     # this file
├── index.md           # catalog of all pages (LLM updates on every ingest)
├── log.md             # append-only log of wiki operations only (ingest, query, lint)
└── *.md               # topic pages
```

`log.md` tracks what goes **into the wiki** — sources ingested, pages created or updated. It is not a project diary. Work sessions, purchases, and build decisions go in `project_logs/` (see `CLAUDE.md`).

## Page types (so far)

| Type | Naming | Purpose |
|---|---|---|
| Goal | `goal_<name>.md` | A desired outcome or quality (the "why" behind constraints and decisions) |
| Component | `component_<name>.md` | A specific hardware part or module |
| Concept | `concept_<name>.md` | A design approach, technology, or tradeoff space |
| Constraint | `constraint_<name>.md` | A hard or soft requirement shaping decisions — should link to the goal it serves |
| Decision | `decision_<name>.md` | A choice made, with rationale — should link to goals and constraints it satisfies |
| Open question | `question_<name>.md` | Something not yet resolved |
| Meta | `meta_<name>.md` | Design process, methodology, and how-we-work notes — not about the product itself |

Pages are atomic: one idea per page. Prefer many small pages over one large one.
Not every page needs to fit a type. If it doesn't fit, just name it sensibly.

## Page format

```markdown
# Title

One-line summary of what this is.

## Facts
- Concrete, sourced information.
- Contradictions with other pages noted explicitly.

## Relevance to this project
Why this matters for the Mondivox build specifically.

## Links
- [[related_page]]
- Source: `external_docs_raw/filename.md`
```

The `## Links` section keeps cross-references explicit. Use `[[wikilink]]` style.

## index.md format

One line per page: `- [[page_name]] — one-line description`

## log.md format

Append-only. Each entry: `## [YYYY-MM-DD] <type> | <title>`

Types: `ingest`, `query`, `lint`

**Always append to the end of the file — never insert earlier.** Entries must remain in chronological order. If a session produces multiple entries, add them all at the bottom in the order they occurred.

Note: `decision` entries belong in `project_logs/`, not here.
