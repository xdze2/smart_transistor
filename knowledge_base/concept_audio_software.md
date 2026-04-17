---
type: concept
---

# Concept: Audio Software Stack

The software layer handling streaming, playback, and GPIO control.

## Facts
- **Squeezelite-ESP32:** firmware turning ESP32 into a Squeezebox receiver; pairs with LMS server.
- **Logitech Media Server (LMS):** self-hosted Docker container; handles Spotify/Deezer API; required for ESP32 path.
- **Mopidy:** Python-based; supports Spotify, SoundCloud, local files; runs on Pi.
- **Volumio:** Pi-focused, full audio OS; community-supported vintage radio projects.
- **DietPi:** ultra-minimal Pi OS; reduces boot time; supports read-only mode to allow hard power cuts.
- **Raspotify:** Spotify Connect daemon for Pi.
- **pleezer:** open-source headless Deezer player for Pi.

## Links
- [[component_brain]]
- [[question_streaming_service]]
- [[question_brain_choice]]
- Source: `internal_docs_raw/brainstorm_vintage_hardware_rebuild.md`
