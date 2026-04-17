# Wiki Schema

Conventions for the `knowledge_base/` directory. Minimal for now — will evolve.

## File structure

```
knowledge_base/
├── WIKI_SCHEMA.md     # this file
├── index.md           # catalog of all pages (LLM updates on every ingest)
├── log.md             # append-only ingest/query log
└── *.md               # topic pages
```

## Page types (so far)

| Type | Naming | Purpose |
|---|---|---|
| Goal | `goal_<name>.md` | A desired outcome or quality (the "why" behind constraints and decisions) |
| Component | `component_<name>.md` | A specific hardware part or module |
| Concept | `concept_<name>.md` | A design approach, technology, or tradeoff space |
| Constraint | `constraint_<name>.md` | A hard or soft requirement shaping decisions — should link to the goal it serves |
| Decision | `decision_<name>.md` | A choice made, with rationale — should link to goals and constraints it satisfies |
| Open question | `question_<name>.md` | Something not yet resolved |

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

Types: `ingest`, `query`, `lint`, `decision`
