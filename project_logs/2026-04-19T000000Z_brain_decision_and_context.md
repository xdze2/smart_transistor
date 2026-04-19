# 2026-04-19 — Brain platform research + project context clarification

## What happened

No hardware touched. Working session focused on clarifying project context, ingesting new docs, and pushing the brain platform decision forward.

Also discussed and rejected Hugo as a doc renderer (MkDocs noted as simpler alternative if ever needed).

## Decisions made

- **FM circuit:** kept as open question. It works and is physically independent from the digital stack — no need to decide before hardware integration. Arguments for and against are documented.
- **Brain platform lean: Raspberry Pi (3A+ or 3B+) + raspotify**, not ESP32.
  - ESP32 killed by portability requirement: LMS server must run somewhere on the network, breaks "works anywhere on WiFi".
  - Pi Zero 2W reliability concern (documented real-world instability with raspotify). Larger Pi preferred for headroom.
  - Boot time constraint relaxed: sleep/wake accepted as alternative to fast cold boot (device is mains-powered, always indoors).
- **Sleep strategy: fake sleep (Option A) as starting point** — mute amp via GPIO, Pi keeps running. OS suspend (Option B, GPIO3 wake) worth attempting after, but WiFi recovery needs testing.
- **Working method: build-first, prototype-driven.** Hands-on testing beats doc reading. Decompose toward the smallest immediately testable step; don't plan for the end goal.

## Project context added

- One-off prototype, not a product. Future flexibility is not a real criterion.
- Mains-powered, always indoors. Battery operation not required.
- Must work anywhere WiFi is available — not home-only. Rules out home-server-dependent solutions.
- Near plug-and-play: one-time WiFi + Spotify setup accepted, no ongoing admin.
- Controls must be self-explanatory to a guest, no explanation needed.

## Meta goals added

- Inspire people and communicate about the build (write-up, photos, etc.)
- Experiment with and learn about AI-assisted design

## Files created

- `knowledge_base/decision_drop_fm.md` → reclassified as `question_open_fm.md` after clarification: FM option remains open
- `knowledge_base/meta_communication_goal.md`
- `knowledge_base/meta_ai_assisted_design.md`
- `knowledge_base/concept_sleep_wake.md`

## Files updated

- `knowledge_base/concept_audio_software.md` — Spotify stack detail (librespot, raspotify, SpotifyEsp32), reliability warning, moOde note
- `knowledge_base/component_brain.md` — Zero 2W reliability concern, ARMv6 restriction
- `knowledge_base/question_brain_choice.md` — full re-analysis with portability constraint; ESP32 weakened; Pi path favoured; SpotifyEsp32 hybrid noted
- `knowledge_base/constraint_boot_time.md` — relaxed: sleep/wake accepted
- `knowledge_base/goal_analog_feel.md` — sleep mode + self-explanatory controls added
- `knowledge_base/goal_simple_streaming.md` — portability + plug-and-play added
- `knowledge_base/meta_engineering_design_process.md` — build-first approach documented
- `knowledge_base/index.md` — new entries: FM question, meta goals, sleep/wake concept, decisions section

## Next step

**Test raspotify on the Pi 4** (hardware already available). Install, connect as Spotify Connect device, play music. Verify reliability. ~20 minutes. Settles the "does Pi + Spotify actually work" question before committing to the platform.
