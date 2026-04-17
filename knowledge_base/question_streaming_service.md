---
type: question
---

# Question: Streaming Service Integration

Which streaming service(s) to support, and via which software path?

## Facts
- Internet radio streams: confirmed target, simplest to implement.
- Spotify: possible via Raspotify (Pi) or LMS + Squeezelite (ESP32).
- Deezer: possible via pleezer (Pi) or LMS (ESP32).
- Local MP3 playback: mentioned as optional.
- ESP32 path requires self-hosted LMS Docker container for Spotify/Deezer — adds infrastructure dependency.
- Final choice of service TBD.

## Links
- [[goal_simple_streaming]]
- [[concept_audio_software]]
- [[question_brain_choice]]
- Source: `internal_docs_raw/brainstorm_mondivox.md`
