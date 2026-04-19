---
type: question
---

# Question: ESP32 vs Raspberry Pi as Brain?

Which computing platform should power the Mondivox build?

## Context

This is a one-off prototype, not a product. "Future flexibility" is not a real criterion — the build that works is better than the build that could theoretically be extended.

## Updated analysis

**ESP32 path — weakened by portability, but a hybrid angle exists**
- Boot time advantage largely gone: sleep/wake is an accepted alternative (see [[constraint_boot_time]]).
- **Requires LMS server for Spotify audio streaming** — LMS must run somewhere on the network. If that's a home NAS, the device stops working elsewhere. Directly violates [[goal_simple_streaming]].
- However: **SpotifyEsp32 library** (Web API wrapper) lets an ESP32 *control* Spotify playback without LMS — skip, play/pause, volume. This is a controller, not a receiver; audio still needs another output device. Not useful standalone.
- Esparagus board is still attractive for integration simplicity (ESP32 + DAC + Amp on one board).
- Viable for internet radio only (no LMS needed for that), but then Spotify is either dropped or requires infrastructure.

**Raspberry Pi path — now more viable**
- Boot time constraint relaxed: sleep mode bridges the gap.
- **Standalone Spotify via librespot/raspotify** — no external server, works on any WiFi network. Meets [[goal_simple_streaming]].
- Pi Zero 2W reliability concern with Spotify (see [[concept_audio_software]]). A Pi 3A+ or Pi 3B+ would be more headroom at modest cost/size increase.
- One-off prototype: no need to optimise for power or size beyond "fits in the shell".

**Current lean:** Pi path, sized for reliability (3A+ or 3B+ rather than Zero 2W), with raspotify for Spotify and a simple internet radio client alongside.

## Original facts
- ESP32 meets original [[constraint_boot_time]] (2–5s); Pi does not (15–30s even optimised).
- ESP32 is more stable (no OS to crash, safe hard power-cut).
- Esparagus board (Sonocotta) bundles ESP32 + DAC + Amp — reduces integration complexity.

## Links
- [[component_brain]]
- [[constraint_boot_time]]
- [[goal_simple_streaming]]
- [[concept_audio_software]]
- Source: `internal_docs_raw/brainstorm_vintage_hardware_rebuild.md`
