---
type: concept
---

# Concept: Sleep / Wake on Raspberry Pi

The device is mains-powered, so power saving is not the goal. The goal is **perceived responsiveness** — it should feel off when not in use and on instantly when needed.

## Options

### Option A — Fake sleep (software mute + amp cut)
- Pi keeps running. On "off": stop playback, cut amp power via GPIO, optionally dim/blank any display.
- Wake: instant — resume playback, restore amp.
- Implementation: simple GPIO + systemd service or Python script.
- Power draw in "sleep": ~300–400 mA (Pi still fully running). Irrelevant for mains use.
- **Simplest. Zero hardware risk. Recommended starting point.**

### Option B — OS suspend (`systemctl suspend`)
- Pi suspends to RAM. Wake via GPIO pin assertion.
- Wake time: ~2–5s. Feels close to instant.
- Risk: WiFi and USB peripherals may not recover cleanly on Pi 3/4 — needs testing.
- Requires a wake trigger: on/off toggle wired to a GPIO, asserting it pulls the Pi out of suspend.
- More satisfying than fake sleep; worth attempting after Option A is working.

### Option C — Full shutdown + hardware power cut
- `shutdown -h`, then external circuit (RTC, latching switch, or power hat) cuts 5V.
- Wake = cold boot: 15–30s. Breaks the "always-ready" feel.
- Not viable unless fast-boot is implemented (significant effort).
- **Ruled out** for this project.

### Option D — Hardware power management hat (Witty Pi, PiJuice)
- Dedicated board that cuts/restores power on schedule or GPIO trigger.
- Same boot-time problem as Option C, plus an extra board.
- **Ruled out** for this project.

## Wake trigger hardware

For Options A and B, the physical on/off control needs to signal the Pi:
- A toggle switch wired to a GPIO pin is the natural fit (Mondivox already has toggle switches).
- Pi polls or uses an interrupt on that GPIO.
- For suspend (Option B): GPIO must be wired to a wake-capable pin — on Pi 3/4, GPIO3 (pin 5) can wake from suspend when pulled low.

## Open questions

- Does WiFi recover cleanly after `systemctl suspend` on the target Pi model? (needs bench test)
- Is Option A "good enough" in practice, or does the Pi visibly running (heat, indicator LED) break the illusion?

## Links

- [[constraint_boot_time]]
- [[goal_analog_feel]]
- [[component_brain]]
- [[concept_hardware_mapping]]
