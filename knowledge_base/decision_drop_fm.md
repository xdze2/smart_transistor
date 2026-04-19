---
type: question
---

# Open Question: Keep or Drop the FM Analog Circuit?

The original FM receiver still works. Whether to keep it is unresolved.

## Arguments for keeping it

- It works, and it's already there — no effort required.
- FM is fully analog and independent from the digital streaming stack; no integration complexity.
- Adds genuine utility (local radio, no internet needed, works during outages).
- Fits the retro feel.

## Arguments for dropping it

- The project goal is internet streaming; FM is a different use case.
- FM reception is poor indoors in most apartments — "works" doesn't mean "useful".
- Keeping FM means maintaining two audio paths and likely more physical controls dedicated to band/frequency selection.
- The retro feel comes from the shell and controls, not the RF front-end.

## Status

Open. FM circuit is functional and physically separate — no need to decide before the build reaches hardware integration.

## Links

- [[goal_simple_streaming]]
- [[goal_analog_feel]]
- [[component_mondivox705]]
