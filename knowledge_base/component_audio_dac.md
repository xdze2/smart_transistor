---
type: component
---

# Component: Audio DAC

I2S DAC converting digital audio to analog signal for the amplifier.

## Facts
- Pi onboard 3.5mm jack is noisy — I2S DAC required for hi-fi quality.
- Options for Raspberry Pi: HiFiBerry DAC+ Zero, Pimoroni Pirate Audio HAT.
- For ESP32: DAC is integrated on the Esparagus board (Sonocotta).
- Separate power supply for the amplifier (vs Pi supply) recommended to avoid ground loop noise.

## Links
- [[goal_good_sound]]
- [[component_brain]]
- [[component_amplifier]]
- Source: `internal_docs_raw/brainstorm_vintage_hardware_rebuild.md`
