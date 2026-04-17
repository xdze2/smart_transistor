# Engineering Design Process

Standard framework for hardware/product development, from problem definition to production.

## Facts

- The process is commonly called the **Engineering Design Process (EDP)** or **Product Development Life Cycle (PDLC)**.
- Six canonical stages:
  1. **Requirements & Specification** (*Cahier des Charges*) — define must-haves vs nice-to-haves; output: measurable criteria list (PDS)
  2. **Conceptual Design** (*Conception*) — explore multiple solutions via feasibility studies; output: selected concept + high-level architecture
  3. **Detailed Design & Modeling** — CAD, Design for Excellence (DFX), Design for Manufacturing; output: blueprints, BOM
  4. **Prototyping** (*Prototypage*) — iterative, low-fidelity → high-fidelity; output: Alpha model
  5. **Testing & Validation** — V&V: *Verification* ("built it right?") vs *Validation* ("built the right thing?"); output: test reports + revisions
  6. **Production & Lifecycle Management** — PLM, from factory to end-of-life

- **Popular frameworks:**
  - **Waterfall** — linear/sequential; one stage fully done before next starts (civil engineering)
  - **Agile/Scrum** — iterative sprints; design/build/test loops (software and tech hardware)
  - **V-Model** — links each design stage to its corresponding test phase

## Relevance to this project

We are using a **lightweight Agile-like approach**: short exploration cycles, no formal Cahier des Charges up front, decisions recorded as they are made rather than pre-planned. The EDP framework provides useful vocabulary (prototype fidelity levels, V&V distinction, BOM) and a reference to check whether we are skipping stages that matter.

The V&V distinction is particularly useful: early hardware experiments are *verification* (does it work as spec'd?); user testing the finished radio will be *validation* (does it feel right?).

## Links

- Source: `external_docs_raw/Engineering Design Process Explained - Google Gemini.md`
