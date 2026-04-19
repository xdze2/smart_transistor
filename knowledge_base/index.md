# Index

## Goals
- [[goal_analog_feel]] — device feels like a physical analog appliance, not a computer
- [[goal_retro_aesthetic]] — retro-futurist look; vintage shell preserved
- [[goal_good_sound]] — hi-fi audio quality, no degradation from digital conversion
- [[goal_simple_streaming]] — streams internet radio / Spotify / Deezer without a phone

## Constraints
- [[constraint_boot_time]] — ready to play within 1–3 seconds of power-on
- [[constraint_no_app_required]] — no smartphone needed for normal use
- [[constraint_stateless_controls]] — each physical control does exactly one thing

## Components
- [[component_mondivox705]] — host radio shell; existing knobs, screen space, speaker
- [[component_brain]] — ESP32 vs Raspberry Pi Zero 2W comparison
- [[component_audio_dac]] — I2S DAC options for hi-fi output
- [[component_amplifier]] — drives the speaker; Esparagus or separate Class-D module

## Concepts
- [[concept_hardware_mapping]] — translating analog controls to GPIO/ADC signals
- [[concept_haptic_controls]] — high-quality knob/switch makers (Elma, Grayhill, NKK…)
- [[concept_audio_software]] — Squeezelite-ESP32, Mopidy, Volumio, Raspotify, pleezer
- [[concept_tangible_ui]] — TUI theory: physical objects as unmediated digital controls
- [[concept_nfc_physical_tokens]] — NFC cards/tiles as phicons for station/playlist selection (Muse Blocks, Vinyl Emulator, Juuke…)
- [[concept_sleep_wake]] — options for Pi sleep/wake: fake sleep, OS suspend, full shutdown (+ trade-offs)

## Open Questions (hardware)
- [[decision_drop_fm]] — keep or drop the FM analog circuit? (functional, independent, but different use case)

## Meta
- [[meta_engineering_design_process]] — EDP/PDLC framework: the six stages of hardware design and how we adapt them here
- [[meta_communication_goal]] — project goal: inspire people, tell the build story
- [[meta_ai_assisted_design]] — project goal: experiment with AI as a design collaborator

## Open Questions
- [[question_brain_choice]] — ESP32 vs Raspberry Pi: which platform?
- [[question_host_enclosure]] — vintage radio shell vs custom-built case
- [[question_screen_sourcing]] — is a screen needed at all? if yes, what fits the aperture?
- [[question_streaming_service]] — internet radio confirmed v1; Spotify/Deezer TBD
- [[question_alarm_clock]] — in main project or a simpler standalone prototype?
