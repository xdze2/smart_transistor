---
type: concept
---

# Concept: Hardware Control Mapping

Translating the original analog controls (knobs, sliders, buttons) into digital signals the brain can read.

## Facts
- **Original potentiometers (analog):** readable via ADS1115 ADC → I2C to Pi/ESP32. Risk: log vs linear curve mismatch requires software correction.
- **Rotary encoders (digital replacement):** cleaner signal; EC11 is common but feels plasticky — high-torque variants (Grayhill, Elma) preferred.
- **Toggle switches / buttons:** wire directly to GPIO pins; straightforward.
- **Tuning dial with string-and-pulley:** attach rotary encoder to main spindle so the needle still moves physically.
- EMI from Wi-Fi can cause audible interference — shielded cables for all audio runs.

## Links
- [[goal_analog_feel]]
- [[constraint_stateless_controls]]
- [[component_mondivox705]]
- [[concept_haptic_controls]]
- Source: `internal_docs_raw/brainstorm_vintage_hardware_rebuild.md`
