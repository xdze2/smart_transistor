# CLAUDE.md — Smart Transistor

Instructions for Claude Code when working in this repository.

## Project summary

DIY hardware project: retrofit a vintage transistor radio (Mondivox 705) into a WiFi streaming music player. Keep the original physical controls. No phone. Fast boot. Streams Spotify/Deezer/webradio.

## Directory layout

| Directory | What it is | Who writes it |
|---|---|---|
| `external_docs_raw/` | Datasheets, articles, reference material | Human (immutable) |
| `internal_docs_raw/` | Brainstorms, raw notes | Human (immutable) |
| `knowledge_base/` | Structured wiki — components, decisions, constraints | Claude |
| `design_docs/` | Design output — specs, architecture, build guide | Claude + Human |
| `project_logs/` | Purchase log, build diary, decision trail | Both |

**Never modify files in `*_raw/` directories.** They are source of truth.

## Knowledge base

See `knowledge_base/WIKI_SCHEMA.md` for conventions.

Short version: markdown files, information-dense, cross-linked with `[[wikilinks]]`. The wiki is a compounding artifact — each ingest updates existing pages, not just adds new ones.

### Ingest workflow

When given a new source to ingest:
1. Read the source
2. Discuss key takeaways if useful
3. Write or update relevant wiki pages (components, constraints, open questions, etc.)
4. Update `knowledge_base/index.md`
5. Append an entry to `knowledge_base/log.md`

### Query workflow

When asked a design question:
1. Read `knowledge_base/index.md` first
2. Pull relevant pages
3. Synthesize an answer
4. If the answer is worth keeping, file it back as a wiki page

## Design docs

Human-readable. Explain decisions and their reasons. Should be usable by someone building the thing months later without remembering the context. Numbered for rough chronological order (`00_`, `10_`, etc.).

## Writing style

Dry. Lightly funny. This is a fun DIY project, not a corporate deliverable. No corporate filler ("leverage", "robust", "seamless"). Brevity over completeness. A single well-placed observation beats a paragraph of hedging.
