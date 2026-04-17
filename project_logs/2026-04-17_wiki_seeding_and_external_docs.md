# 2026-04-17 — Wiki seeding + external docs ingest

## What happened

Two sessions today (second one after a /clear).

**Session 1 — initial wiki seeding**

Ingested the two internal brainstorm docs (`brainstorm_mondivox.md`, `brainstorm_vintage_hardware_rebuild.md`) and a round of user clarifications. Created 17 wiki pages covering goals, constraints, components, concepts, and open questions. Key clarifications recorded:

- Host enclosure not locked — Mondivox 705 is a strong candidate but not decided
- Screen is optional, pending tangible interface research
- Internet radio confirmed for v1; Spotify/Deezer are nice-to-have
- Alarm clock moved out of scope as a potential standalone project
- Speaker quality target: small portable room speaker

**Session 2 — external docs ingest**

Processed a batch of 8 external docs added to `external_docs_raw/`. Two new concept pages created:

- `concept_tangible_ui.md` — TUI theory (Hiroshi Ishii / MIT Media Lab). Validates the screenless, one-knob-one-function design direction. Key concept: the "phicon" (physical icon = tangible object holding a reference to a digital entity).
- `concept_nfc_physical_tokens.md` — NFC/RFID music players as precedents: SENIC Muse Blocks (commercial), Sonos Vinyl Emulator (DIY RPi + NFC cards), Juuke (elderly/children RFID box), NFC Floppy Disk (Arduino + MFRC522). Hardware notes: MFRC522 SPI module, metal enclosures interfere with reads, tags <€0.50 each.

Cross-links added to `question_screen_sourcing` and `concept_haptic_controls`. `external_docs_raw/README.md` now has a full index of all 10 source files.

## Decisions made

- NFC tokens are a plausible v2 addition for preset stations/playlists — not in v1 scope, but worth keeping in mind during enclosure design (needs a non-metallic aperture for the reader).
- TUI theory gives a principled reason to *not* add a screen: purpose-built physical appliances work better without one.

## Files created / updated

- `knowledge_base/concept_tangible_ui.md` — new
- `knowledge_base/concept_nfc_physical_tokens.md` — new
- `knowledge_base/concept_haptic_controls.md` — added TUI link
- `knowledge_base/question_screen_sourcing.md` — added TUI + NFC token context
- `knowledge_base/index.md` — two new concept entries
- `knowledge_base/log.md` — two ingest entries
- `external_docs_raw/README.md` — full source index

## Next steps

- Open the Mondivox 705, take photos, measure internals (especially the aperture for a potential screen or NFC cutout)
- Start a `design_docs/` page on the control mapping (knob/switch → GPIO/ADC)
- Decide on brain: ESP32 vs RPi Zero 2W — this unblocks most component choices
