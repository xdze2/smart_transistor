---
type: constraint
---

# Constraint: Ready-to-Play Feel (Boot / Wake)

The device should feel immediately available — no waiting, no staring at a boot screen.

## Facts
- The device is always plugged into 220V indoors. Battery operation is not a requirement.
- **Sleep/wake is an accepted alternative to fast cold boot.** A deep sleep that wakes in 1–2s satisfies the "always-ready" feeling just as well as a 3s cold boot.
- Cold boot of 15–20s (Pi path) is acceptable *if* the device is left in sleep mode between uses rather than hard power-cycled.
- Hard power-cut + fast cold boot (ESP32 path) is still a valid approach, but no longer the only one.
- A 30–45s full Linux boot from cold with no sleep mode would still break the illusion — that remains unacceptable.

## Links
- [[goal_analog_feel]]
- [[component_brain]]
- Source: `internal_docs_raw/brainstorm_vintage_hardware_rebuild.md`
