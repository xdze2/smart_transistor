---
type: concept
---

# Concept: Audio Software Stack

The software layer handling streaming, playback, and GPIO control.

## Facts

### Spotify integration — three paths (overview)
- **eSDK (Spotify Embedded SDK):** official C library used by Bose, Sonos, etc. Handles streaming, DRM, ZeroConf. Restricted to approved commercial partners — not accessible for personal/DIY projects.
- **librespot / raspotify (DIY path):** open-source reverse-engineered implementation. Device appears as a Spotify Connect receiver. Audio streams from Spotify's servers directly to the device — the phone is just a remote, not the audio source. **This is the path for this project.**
- **Web API (controller path):** controls playback on another device. No audio streaming. Useful for custom remotes (e.g. ESP32 with buttons).
- All hardware streaming paths require **Spotify Premium**.
- Spotify Connect = cloud-based; unlike Bluetooth, the phone sends commands, not audio.

### Spotify stack (Pi path)
- **librespot:** open-source Spotify Connect client library (Rust). Reverse-engineered protocol; Premium required. Actively maintained by community. Spotify's ToS technically forbids it, but no enforcement action known. MIT license.
- **raspotify:** thin systemd daemon wrapping librespot for headless Debian/Pi use. One-liner install. ARM64/armhf only — does **not** support ARMv6 (Pi Zero v1 is out). Intended for headless use; not a full audio OS.
- **spotifyd:** alternative stripped-down librespot daemon; better suited for desktop OS setups. Reported ARM binary architecture mismatch on Pi 3 — may require compiling from source (slow, unreliable). Less battle-tested on Pi than raspotify.
- **Reliability concern:** real-world reports of Pi Zero 2W + raspotify/librespot being unstable — 7/10 playback failures, service crashes, connect timeouts. May be a Zero 2W CPU headroom issue rather than a software fault. Separately confirmed working well on Pi 3 (Raspbian 64-bit, headless).

### Spotify stack (ESP32 path)
- **Squeezelite-ESP32:** firmware turning ESP32 into a Squeezebox receiver; pairs with LMS server.
- **Logitech Media Server (LMS):** self-hosted Docker container; handles Spotify/Deezer API; required for ESP32 path. Not standalone — tied to a home server, breaks portability.
- **SpotifyEsp32 (FinianLandes):** Arduino library wrapping the Spotify Web API for ESP32. Controls playback (skip, play/pause, get track info, volume) via HTTPS API calls. **Does NOT stream audio** — it is a remote controller, not a receiver. Use case: ESP32 acts as a physical controller while audio plays through another Spotify Connect device, or alongside a separate audio output. Requires Spotify Developer app credentials (Client ID + Secret). Tokens stored in flash (SPIFFS). Updated Feb 2026 to align with new Spotify API.

### Other Pi options
- **Mopidy:** Python-based; supports Spotify, SoundCloud, local files; runs on Pi.
- **Volumio:** Pi-focused, full audio OS; known Pi Zero 2W boot issues reported.
- **DietPi:** ultra-minimal Pi OS; reduces boot time; supports read-only mode to allow hard power cuts.
- **pleezer:** open-source headless Deezer player for Pi.
- **moOde audio player:** recommended by raspotify maintainer as a turnkey Pi audio solution with Spotify Connect support.

## Links
- [[component_brain]]
- [[question_streaming_service]]
- [[question_brain_choice]]
- Source: `internal_docs_raw/brainstorm_vintage_hardware_rebuild.md`
- Source: `external_docs_raw/librespot-orglibrespot Open Source Spotify client library.md`
- Source: `external_docs_raw/dtcooperraspotify A Spotify Connect client that mostly Just Works™.md`
- Source: `external_docs_raw/Raspberry Pi Zero 2 W as a Spotify Connect player. Does it work for you  rraspberry_pi.md`
- Source: `external_docs_raw/Run Spotify on your Raspberry Pi. Play your Spotify library from your Pi  by Gerrit Stapper  NEW IT Engineering  Medium.md`
- Source: `external_docs_raw/FinianLandesSpotifyEsp32 This is a library to connect to and control spotify using an esp.md`
- Source: `external_docs_raw/Connecting Devices to Spotify - Google Gemini.md`
