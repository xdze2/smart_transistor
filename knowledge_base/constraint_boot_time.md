---
type: constraint
---

# Constraint: Boot Time ≤ 3 seconds

The device must be ready to play within 1–3 seconds of power-on.

## Facts
- A 30–45s Linux boot destroys the "always-ready appliance" feeling.
- ESP32 boots in 2–5s with no OS overhead — meets this constraint natively.
- Raspberry Pi Zero 2W with DietPi + read-only mode + service pruning: ~15–20s. Does **not** meet the strict target.
- Pi boot can be optimised further but requires significant effort.

## Links
- [[goal_analog_feel]]
- [[component_brain]]
- Source: `internal_docs_raw/brainstorm_vintage_hardware_rebuild.md`
