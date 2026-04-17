---
type: concept
---

# Concept: Tangible User Interface (TUI)

A design paradigm where physical objects are computationally coupled to digital information — the physical state *is* the interface state.

## Facts

- Coined by Hiroshi Ishii (MIT Media Lab, 1997). Original name: "Graspable User Interface".
- Core idea: **physical representations embody both data and control** — touching/moving the object *is* interacting with the digital system.
- Key distinction from GUI: in a TUI the coupling between cognitive intent and system response is *unmediated* — the user applies known physical intuition rather than learning an abstract visual language.
- TUIs are typically single-purpose by design (one application per device), which is a strength not a limitation for appliances.
- "Phicon" = physical icon: a tangible object that holds a reference to a digital entity (e.g. an NFC card that represents a playlist).
- TUIs have proven especially effective for: elderly users, children, domain experts who already have strong physical intuitions (musicians, craftspeople).
- Usability depends on design quality and task fit, not on tangibility being inherently intuitive.

## Relevance to this project

The Mondivox build *is* a TUI: each physical knob, switch, and (potentially) token maps 1:1 to a digital action with no intermediate menu or screen. The constraint [[constraint_stateless_controls]] is a direct expression of TUI principles. Understanding TUI theory validates the design direction and warns against feature-creep toward GUI patterns (e.g. adding a touchscreen with a menu tree).

The "phicon" concept is directly applicable if physical tokens (NFC cards/tiles) are used to select radio stations or playlists — see [[concept_nfc_physical_tokens]].

## Links

- [[goal_analog_feel]]
- [[constraint_stateless_controls]]
- [[concept_haptic_controls]]
- [[concept_nfc_physical_tokens]]
- Source: `external_docs_raw/Tangible user interface - Wikipedia.md`
- Source: `external_docs_raw/Bridging Digital and Physical Objects - Google Gemini.md`
