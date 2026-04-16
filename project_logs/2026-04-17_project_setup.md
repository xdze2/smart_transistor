# 2026-04-17 — Project setup & tooling

## What happened

First working session. No hardware touched. Laid the groundwork for AI-assisted design.

Defined the repo structure and the workflow: raw docs go in `*_raw/`, Claude maintains a structured wiki in `knowledge_base/`, human-readable output lands in `design_docs/`.

The wiki pattern is lifted from Karpathy's LLM Wiki — persistent, compounding, LLM-maintained. The idea: don't re-derive knowledge from scratch on every question, build it up incrementally as sources and decisions accumulate.

## Files created

- `README.md` — expanded with project description and repo structure
- `CLAUDE.md` — instructions for Claude: directory roles, ingest/query workflows, writing style
- `knowledge_base/WIKI_SCHEMA.md` — minimal wiki conventions (page types, format, index/log structure)

## Decisions made

- `knowledge_base/` is Claude's territory: dry, dense, cross-linked
- `design_docs/` is human-readable output: explains decisions and how to build the thing
- Hardware constraints removed from `CLAUDE.md` — they belong in the wiki, not the tooling config

## Next steps

- First ingest: process `internal_docs_raw/brainstorm_mondivox.md` to seed the knowledge base
- Open the radio, take photos, measure the internals
