# Smart Transistor

Take an old transistor radio — the kind your grandparents ignored in the corner — and turn it into a WiFi streaming music player. Keep the knobs. Keep the sliders. Keep the vaguely retro soul. Replace everything else.

## What this is

A DIY hardware project. The goal: a connected music player with physical controls, no phone required, that boots fast enough to feel like an appliance rather than a computer. Streams Spotify, Deezer, and/or internet radio. Configured once via Bluetooth, then left alone.

The current candidate host body is a **Mondivox 705**. It has good knobs. Host enclosure is not yet locked — a custom case is also on the table.

## What this is not

- A professional product
- A clean build (there will be hot glue)
- Something you could sell

## Features (target)

- Physical controls only — volume slider, channel selector, on/off
- No app, no screen unlock, no notifications
- Fast boot (target: under 5 seconds)
- WiFi streaming: Spotify / Deezer / webradio
- Wi-Fi setup once via web UI or config file; no app needed after that
- Fits inside the original case

## Repository structure

```
external_docs_raw/   # datasheets, articles, reference material — read only
internal_docs_raw/   # brainstorms, notes, raw thinking — read only
knowledge_base/      # structured wiki, LLM-maintained, information-dense
design_docs/         # actual design output — specs, schematics, build instructions
project_logs/        # purchase log, build diary, decisions made
```

## AI-assisted design

The `knowledge_base/` is maintained by Claude as a persistent, structured wiki — components, tradeoffs, constraints, open questions. The idea is lifted from [Karpathy's LLM Wiki pattern](external_docs_raw/karpathy_llm-wiki.md): raw sources go in, structured knowledge comes out, nothing gets re-derived from scratch on every question.

Design decisions and their reasons are tracked in `design_docs/` and `project_logs/`.

## Status

- [x] Bought the radio
- [ ] Open it without breaking it
- [ ] Figure out what fits inside
- [ ] Pick a brain (ESP32 vs Pi)
- [ ] First sound out
