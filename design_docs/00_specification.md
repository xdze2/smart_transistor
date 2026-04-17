# 00 — Specification

Project specification for the Smart Transistor / Mondivox 705 rebuild.

---

## 1. Purpose

Build a connected music player that looks and behaves like a physical analog appliance. Not a smart speaker. Not a computer with a screen. A radio — one that happens to stream the internet.

---

## 2. Goals

### G1 — Analog feel
The device must feel like a dedicated appliance: always ready, physical controls only, no menus, no unlock screen. The interaction model is a 1970s transistor radio, not a smartphone.

### G2 — Good sound quality
Audio output quality: small portable room speaker level. Clear enough for a quiet room; no stereo required. The original speaker may be reused or replaced — this is a design-phase decision.

### G3 — Retro-futurist aesthetic
The device should look like a vintage radio that has been quietly upgraded. Any new parts must not clash with the vintage aesthetic. The host shell — vintage radio or custom case — is a conception-phase decision.

### G4 — Simple streaming
Streams internet radio without a phone, companion app, or complex UI. Spotify/Deezer is a nice-to-have for v1. Local MP3 playback is out of scope.

---

## 3. Constraints

### C1 — Boot time ≤ 3–5 seconds
The device must be ready to play within 3–5 seconds of power-on. A long boot breaks the appliance illusion. This constraint is a primary driver of the brain platform choice.

### C2 — No phone required for normal use
Day-to-day operation (power, volume, station selection) works without any smartphone or app. Exceptions: initial Wi-Fi setup and streaming-service credential entry (one-time admin).

### C3 — Stateless controls
Each physical control does exactly one thing. No mode-switching, no multi-function buttons, no contextual behavior.

**Required controls:** hard on/off, volume, station/channel selection.  
**Optional controls:** shuffle, play/pause, skip next/previous.  
**Explicitly excluded:** search, playlist management, fast-forward/rewind, time/alarm setting.

---

## 4. Open questions (at specification stage)

These are not resolved yet and will be addressed in conception:

| ID | Question | Impact |
|---|---|---|
| Q1 | ESP32 vs Raspberry Pi? | Boot time, Spotify support, integration complexity |
| Q2 | Vintage shell vs custom case? | Aesthetic, geometry constraints |
| Q3 | Screen — needed or not? | Aesthetic risk, control feedback |
| Q4 | Streaming service: internet radio only, or Spotify/Deezer too? | Software stack, infrastructure |
| Q5 | Alarm clock — in scope or separate project? | Scope |

See `knowledge_base/question_*.md` for detailed analysis of each.

---

## 5. Out of scope (v1)

- Local MP3 playback
- Alarm clock
- Bluetooth audio output
- Multi-room audio
- Voice control
- Any form of companion app

---

## 6. Success criteria

The build is successful when:

1. Power-on to audio playing in ≤ 5 seconds.
2. Station can be changed using a physical control only.
3. Volume can be adjusted using a physical control only.
4. No phone is needed after initial Wi-Fi setup.
5. The device fits inside the chosen host enclosure, with original external controls preserved or replaced with equivalents.
6. Audio quality: no audible interference, no distortion at normal listening volume.
