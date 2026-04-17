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

## Open Questions
- [[question_brain_choice]] — ESP32 vs Raspberry Pi: which platform?
- [[question_screen_sourcing]] — ultra-wide display for the Mondivox 705 aperture
- [[question_streaming_service]] — Spotify vs Deezer vs internet radio; LMS dependency?
