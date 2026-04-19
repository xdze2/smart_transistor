---
type: goal
---

# Goal: Simple Streaming

The device streams internet radio and/or Spotify/Deezer without needing a phone, app, or complex UI.

## Facts
- Internet connectivity is required — local MP3-only is not a viable use case.
- Target sources: internet radio streams (confirmed), Spotify/Deezer (TBD), local MP3 (out of scope for v1).
- Alarm clock: out of main scope; noted as a potential simpler standalone project.
- **Works anywhere WiFi is available** — not locked to a home network. The device should work at a friend's place, in a rental, wherever. This rules out solutions that depend on a local server (e.g. LMS/Docker on a home NAS).
- **Near plug-and-play:** initial setup (WiFi credentials + Spotify login) is acceptable, but should be minimal and done once. No ongoing admin.
- Wi-Fi setup and Spotify credential entry are accepted one-time exceptions to the no-phone rule.

## Links
- [[constraint_no_app_required]]
- [[question_streaming_service]]
- [[concept_audio_software]]
- Source: `internal_docs_raw/brainstorm_mondivox.md`
