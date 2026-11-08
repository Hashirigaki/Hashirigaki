# Hashirigaki Lab

**Exploring cognitive dynamics and building inspectable AI workflows.**

I work on computational approaches to memory and cognition, and on practical tools that help humans and AI agents work together. My interests include state-space models, chaotic dynamical systems, nonlinear analysis, network structure, and synchronization.

This portfolio separates conceptual simulations, implemented prototypes, and work awaiting a public release. Each project states what it currently demonstrates and how to inspect or reproduce it.

## Computational & Cognitive Dynamics

### [FDR — Conceptual Simulation](https://github.com/Hashirigaki/fdr-conceptual-simulation)

**Flow Dissipation & Reconvergence · v0.5 showcase**

How can the shape of a state space influence dispersion, movement between potential wells, and return toward an initial region? This Python simulation compares three barrier heights with an external cue switched off or on. Two demonstrations show a standard regime and a deliberately engineered diffuse-stress regime.

- **Explore:** [Standard video](https://github.com/Hashirigaki/fdr-conceptual-simulation/blob/main/outputs/showcase_v0.5/FDR_v0_5_standard_6panel.mp4) · [Diffuse-stress video](https://github.com/Hashirigaki/fdr-conceptual-simulation/blob/main/outputs/showcase_v0.5/FDR_v0_5_diffuse_stress_6panel.mp4) · [Figures and data](https://github.com/Hashirigaki/fdr-conceptual-simulation/tree/main/outputs/showcase_v0.5)
- **Reproduce:** [Python source](https://github.com/Hashirigaki/fdr-conceptual-simulation/blob/main/src/fdr_v0_5_showcase.py) · [Notebook](https://github.com/Hashirigaki/fdr-conceptual-simulation/blob/main/notebooks/FDR_v0.5_Showcase_Colab.ipynb) · [Verification and limits](https://github.com/Hashirigaki/fdr-conceptual-simulation/blob/main/docs/verification.md)
- **Scope:** a conceptual simulation. It does not establish chaotic dynamics, biological memory mechanisms, or neuroscience validity. Local Python and Jupyter execution have been checked; Google Colab cloud execution remains untested.

### Related modeling work

| Model | Question | Current portfolio status |
|---|---|---|
| Barabási–Albert Network Modeling | How can preferential attachment produce heterogeneous network structure? | Existing code reported; source review and public release pending. |
| FitzHugh–Nagumo | How do simple excitable units produce pulses and recovery? | Prior visualization work reported; source review and public release pending. |
| Kuramoto Model | How do interacting oscillators become synchronized? | Prior visualization work reported; source review and public release pending. |

These are established models. Their separate artifacts will be linked after review; they are not included in the FDR release.

## Applied AI Agents

### [Appointment Agent](https://github.com/Hashirigaki/appointment-agent-google)

An ontology-based appointment workflow using Google ADK, Gemini, and JSON or Firestore state storage. The workflow records its progress and pauses for human slot approval before confirmation. Provider responses are mocked; the prototype makes no real bookings.

[Setup and runnable demo](https://github.com/Hashirigaki/appointment-agent-google#local-setup) · [Demo walkthrough](https://github.com/Hashirigaki/appointment-agent-google/blob/main/docs/demo-script.md)

### [CommonThread](https://github.com/Hashirigaki/commonthread-webmcp)

A shared workspace where humans and agents can read and contribute to the same persistent project history. The v0.1 prototype includes one project, one thread, a local JSON store, an OpenAI participant, and WebMCP `read_thread` / `post_entry` tools. Multiple projects, cross-thread retrieval, and trusted agent identity are future work.

[Run locally](https://github.com/Hashirigaki/commonthread-webmcp#run-locally) · [Current demonstration](https://github.com/Hashirigaki/commonthread-webmcp#what-v01-demonstrates)

## Developer Tools

### [ContextGate](https://github.com/Hashirigaki/contextgate-datahub-agent)

A deterministic prototype for deciding whether metadata context should be allowed, blocked, or reviewed. Fixture Replay Mode writes decision receipts and verifies them by reading them back. Live DataHub integration is future work; the implemented replay uses no LLM or external service.

[CLI and setup](https://github.com/Hashirigaki/contextgate-datahub-agent#cli) · [Replay evidence](https://github.com/Hashirigaki/contextgate-datahub-agent/blob/main/docs/evidence/fixture-replay.md)

## Working approach

- **Reproducibility:** runnable source, parameters, examples, and explicit verification boundaries.
- **Traceability:** inspectable state, decisions, and human intervention.
- **Research transparency:** clear separation between a visual illustration and empirical evidence.

**Tools:** Python, NumPy, Matplotlib, Jupyter, JavaScript / Node.js, WebMCP, Google ADK, and Firestore.
