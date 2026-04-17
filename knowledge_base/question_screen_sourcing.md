---
type: question
---

# Question: Is a Screen Needed at All?

A screen is not required if the physical controls give sufficient feedback on their own.

## Facts
- Core rationale for a screen: feedback from controls (e.g. current station, volume level).
- If controls are well-designed (stateless, self-evident), a screen may add no value — and adds aesthetic risk.
- TUI theory (see [[concept_tangible_ui]]) supports screenless design: purpose-built physical appliances benefit from *not* having a screen — it forces clear physical affordances and avoids the GUI complexity trap.
- NFC token approach (see [[concept_nfc_physical_tokens]]) could replace a "now playing" screen: the token *is* the visible label for what's playing.
- If a screen is used, it must fit the Mondivox 705 aperture: ≈10.5 × 3 cm, usable width ~7.5 cm.
- Display leads (if needed):
  - Youritech 2.7" bar-style: https://www.youritech.com/products/2-7-inch-bar-style-displays/
  - Youritech 4" OLCD 960×160 MIPI AMOLED: https://www.youritech.com/products/4-inch-olcd-display-960x160-mipi-amoled-display-with-capacitive-touch.html
  - Multi-display + I2C multiplexer: complex, not preferred.
- Alternative: keep original frequency-range backlight as a fixed cosmetic element.
- Prototype-first: validate controls without a screen before committing.

## Links
- [[goal_retro_aesthetic]]
- [[component_mondivox705]]
- [[concept_tangible_ui]]
- [[concept_nfc_physical_tokens]]
- Source: `internal_docs_raw/brainstorm_mondivox.md`
