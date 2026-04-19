---
type: component
---

# Component: Brain (microcontroller / SBC)

The computing unit running the audio software and GPIO control logic.

## Facts
- Two main candidates:

**ESP32**
- Boot time: 2–5 s. Meets [[constraint_boot_time]].
- No OS; runs firmware directly (e.g. Squeezelite-ESP32).
- Requires an external server (LMS / Docker) for Spotify/Deezer — not standalone.
- Very low power; safe to hard-cut power (no SD corruption).
- Specific board: **Esparagus** by Sonocotta — ESP32 + DAC + Amp on one board.

**Raspberry Pi Zero 2W**
- Boot time: 15–30 s (optimised with DietPi + read-only mode). Does **not** meet [[constraint_boot_time]].
- Standalone: handles Spotify via raspotify/librespot, Deezer via pleezer.
- Fits in any vintage shell.
- Paired with HiFiBerry DAC+ Zero or Pimoroni Pirate Audio.
- **Reliability concern:** real-world reports of significant Spotify Connect instability on Zero 2W — frequent service crashes and playback failures. Possibly CPU headroom issue. Larger Pi (3B+, 4, 5) likely more stable but worse on boot time and power/heat.
- raspotify does **not** support Pi Zero v1 (ARMv6). Zero 2W (ARMv8/arm64) is fine.

## Links
- [[constraint_boot_time]]
- [[component_audio_dac]]
- [[concept_audio_software]]
- [[question_brain_choice]]
- Source: `internal_docs_raw/brainstorm_vintage_hardware_rebuild.md`
