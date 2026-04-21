# Log

## [2026-04-17] ingest | brainstorm_mondivox + brainstorm_vintage_hardware_rebuild
Initial ingest from two brainstorm documents. Created 17 pages: 4 goals, 3 constraints, 4 components, 3 concepts, 3 questions.

## [2026-04-17] ingest | external_docs batch (TUI theory + NFC physical tokens)
Ingested 8 new external docs. Created 2 new pages: [[concept_tangible_ui]] (TUI theory, Ishii/MIT, phicon concept) and [[concept_nfc_physical_tokens]] (NFC/RFID music players: Muse Blocks, Vinyl Emulator, Juuke, NFC Floppy). Updated [[concept_haptic_controls]], [[question_screen_sourcing]] with cross-links. Updated index.md and external_docs_raw/README.md. Skipped: Argument map (not project-relevant), karpathy_llm-wiki (meta/methodology, not content), Hipster PDA (tangential).

## [2026-04-17] ingest | Engineering Design Process Explained - Google Gemini
Added new category "Meta" (design process / methodology). Created [[meta_engineering_design_process]]: EDP/PDLC six-stage framework, V&V distinction, Waterfall/Agile/V-Model comparison. Updated WIKI_SCHEMA.md with Meta type, index.md with new section.

## [2026-04-17] ingest | user clarifications
Updated 6 pages, added 2 new questions. Key changes: host enclosure is not locked (Mondivox 705 is a candidate); screen is optional pending tangible interface research; internet radio confirmed v1, Spotify/Deezer nice-to-have; alarm clock moved out of scope as potential standalone project; speaker quality target defined as small portable room speaker.

## [2026-04-19] ingest | user clarifications (FM decision + meta goals)
Created 3 new pages: [[decision_drop_fm]] (rationale for dropping the FM analog circuit), [[meta_communication_goal]] (project goal: inspire and communicate), [[meta_ai_assisted_design]] (project goal: experiment with AI-assisted design). Added "Decisions" category to index.md. Updated [[meta_engineering_design_process]] cross-links.

## [2026-04-19] ingest | Spotify client docs (librespot, raspotify, Pi Zero 2W reliability)
Updated [[concept_audio_software]]: added detailed Spotify stack section (librespot, raspotify, spotifyd, moOde), ESP32 path clarification, real-world Pi Zero 2W reliability warning. Updated [[component_brain]]: added Zero 2W Spotify instability note and ARMv6 restriction. Sources: 3 new external docs.

## [2026-04-19] ingest | user context clarifications (scope, power, portability, controls)
Updated [[constraint_boot_time]]: relaxed — sleep/wake accepted as alternative to fast cold boot. Updated [[goal_analog_feel]]: added sleep mode and self-explanatory controls. Updated [[goal_simple_streaming]]: added portability requirement (works on any WiFi, not home-only) and plug-and-play. Updated [[question_brain_choice]]: full re-analysis — ESP32 weakened by LMS portability issue, Pi path now favoured (3A+/3B+ for reliability); added one-off prototype context.

## [2026-04-19] ingest | SpotifyEsp32 library (Web API controller for ESP32)
Updated [[concept_audio_software]]: added SpotifyEsp32 entry — clarified it is a Web API *controller* (skip/play/volume), not an audio receiver; does not stream audio, no LMS needed. Updated [[question_brain_choice]]: noted hybrid angle (ESP32 as controller) but confirmed it doesn't solve standalone streaming. Source: `external_docs_raw/FinianLandesSpotifyEsp32...md`.

## [2026-04-19] ingest | Gerrit Stapper — Run Spotify on Raspberry Pi (Medium)
Updated [[concept_audio_software]]: raspotify confirmed working on Pi 3 (64-bit headless); spotifyd noted as unreliable on Pi ARM (architecture mismatch, compile from source required).

## [2026-04-19] query | Pi sleep/wake options
Created [[concept_sleep_wake]]: four options (fake sleep, OS suspend, full shutdown, power hat). Options C and D ruled out. Option A recommended as starting point; Option B worth testing. Added GPIO wake trigger notes. Updated index.

## [2026-04-22] ingest | Connecting Devices to Spotify — Gemini overview
Updated [[concept_audio_software]]: added top-level three-path overview (eSDK, librespot, Web API); clarified Spotify Connect is cloud-based (phone sends commands, not audio); named eSDK as the commercial-only official path.

## [2026-04-22] lint | chronological sort + schema update
Sorted all entries into chronological order. Added append-only rule to WIKI_SCHEMA.md.
