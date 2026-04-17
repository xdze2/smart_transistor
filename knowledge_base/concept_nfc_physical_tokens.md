---
type: concept
---

# Concept: NFC Physical Tokens for Music Selection

Using physical objects embedded with NFC (or RFID) tags as tangible "phicons" to select and trigger digital music streams — no screen, no scrolling, no app.

## Facts

- NFC tags are passive, cheap (<€0.50 each), tiny — can be embedded in cards, tiles, floppy disks, cassettes, wooden blocks, etc.
- Reading range: 1–3 cm for typical MFRC522/PN532 modules; requires deliberate placement (no accidental triggers).
- **Common implementations:**
  - **SENIC Muse Blocks** (commercial): 8×8 cm NFC tiles with printed album art; tap to phone or dedicated reader triggers Spotify/Apple Music playlist. Sold with a wall-mounted ash wood bar. Closest commercial equivalent to what this project could do.
  - **Sonos Vinyl Emulator** (DIY, Mark Hankinson): cardboard mini album art cards with NFC tags → Raspberry Pi → Sonos API. ~100 cards for £25 in printing. Also adapted for cassette boxes.
  - **NFC Floppy Disk** (DIY, Coconauts): NFC sticker inside old floppy disk → Arduino MFRC522 → Python script → game launcher. LEGO structure replaced metallic shell (metal interfered with NFC reads).
  - **Juuke** (DIY): dedicated music player for elderly/children; picture cards placed in a slot trigger playback — removes smartphone complexity entirely.
- Hardware path: MFRC522 module (SPI, 13.56 MHz, ISO 14443A/MIFARE/NTAG) is the most documented option. PN532 also widely used.
- Metal enclosures interfere with NFC — reader must be positioned away from metallic shells or use a non-metallic aperture.
- Software: Arduino reads UID via serial → host script maps UID to action. On RPi: Python `nfcpy` or similar library reads tags directly.
- Each token gets its UID enrolled once; mapping list updated manually as collection grows.

## Relevance to this project

A token-based selection mechanism could solve [[question_streaming_service]] input without a screen: place a card → plays that station or playlist. This directly embodies [[goal_analog_feel]] (physical ritual, like putting on a record) and [[constraint_no_app_required]].

The Mondivox shell has the volume knob and tuner dial for navigation already; tokens could be an *optional* layer for preset stations/playlists, not a replacement for knobs. The metallic Mondivox 705 casing is a concern — the NFC reader would need to be positioned at a non-metallic aperture or behind a small cutout.

Open question: does this complicate the build scope for v1? May be better as v2 addition once core streaming works.

## Links

- [[goal_analog_feel]]
- [[constraint_no_app_required]]
- [[constraint_stateless_controls]]
- [[concept_tangible_ui]]
- [[question_streaming_service]]
- [[component_brain]]
- Source: `external_docs_raw/Rico Bacellar - Portfolio - SENIC Muse Blocks.md`
- Source: `external_docs_raw/Sonos  Spotify Vinyl Emulator — Raspberry Pi Official Magazine.md`
- Source: `external_docs_raw/NFC Floppy Disk Game Launcher  The Coconauts Blog.md`
- Source: `external_docs_raw/Juuke - a RFID Music Player for Elderly and Kids  10 Steps (with Pictures) - Instructables.md`
- Source: `external_docs_raw/Bridging Digital and Physical Objects - Google Gemini.md`
