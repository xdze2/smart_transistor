---
type: question
---

# Question: Streaming Service Integration

Which streaming service(s) to support, and via which software path?

## Facts
- Internet connectivity is required — MP3-only is not a viable use case.
- Internet radio streams: confirmed v1 target, simplest to implement.
- Spotify/Deezer: nice-to-have; choice of service and implementation path TBD.
- Local MP3: out of scope for v1.
- ESP32 path requires self-hosted LMS Docker container for Spotify/Deezer — adds infrastructure dependency.
- Alarm clock: out of main scope; noted as a candidate for a simpler standalone project.

## Links
- [[goal_simple_streaming]]
- [[concept_audio_software]]
- [[question_brain_choice]]
- Source: `internal_docs_raw/brainstorm_mondivox.md`
