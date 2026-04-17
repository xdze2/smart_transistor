---
type: question
---

# Question: ESP32 vs Raspberry Pi as Brain?

Which computing platform should power the Mondivox build?

## Facts
- ESP32 meets [[constraint_boot_time]] (2–5s); Pi does not (15–30s even optimised).
- ESP32 requires an external LMS server for Spotify/Deezer; Pi is standalone.
- ESP32 is more stable (no OS to crash, safe hard power-cut).
- Esparagus board (Sonocotta) bundles ESP32 + DAC + Amp — reduces integration complexity.
- Pi path offers more flexibility for future features (screen, complex UI, etc.).

## Links
- [[component_brain]]
- [[constraint_boot_time]]
- [[concept_audio_software]]
- Source: `internal_docs_raw/brainstorm_vintage_hardware_rebuild.md`
