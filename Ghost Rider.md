# SQ-2046 Programmable Analog Sequencer

The SQ-2046 is a browser-based, three-track step sequencer and groovebox inspired by classic vintage hardware workflows. It combines a highly customisable scheduling engine with an authentic sound signature, bridging the gap between web applications and studio hardware environments.

---

## Technical Capabilities

The application functions both as a standalone virtual instrument and a central routing brain for external equipment.

*   **Dual Synthesizer Voices (Tracks A & B):** Features persistent web-audio oscillator engines configured with selectable waveforms (sawtooth, square, triangle, sine) and a noise generator mix.
*   **Acoustic Squelch Engine (303-style Architecture):** Includes programmable per-step **Slide (Legato Portamento)** and **Accent** options. When steps are tied via Slide, the engine glides the pitch smoothly without re-triggering the filter envelope. The global Accent control governs volume spikes and aggressive, snappy envelope decay adjustments.
*   **Rhythm Generator (Track C):** A dedicated drum synthesizer path with integrated step controls for a Bass Drum, Snare Drum, and High-Hat with dynamic velocity filtering.
*   **Master Effects Bus:** Includes a global low-pass filtered delay circuit mathematically locked to divisions of the master tempo (1/4, 1/8, 1/8 Dotted, and 1/16 notes) alongside adjustable feedback and mix controls.

---

## System Workflow & Architecture

```text
                       ┌─────────────────────────┐
                       │  Master BPM Clock &     │
                       │  Global Transport Bus   │
                       └────────────┬────────────┘
                                    │
            ┌───────────────────────┼───────────────────────┐
            ▼                       ▼                       ▼
   ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
   │ Track A (VCO 1) │     │ Track B (VCO 2) │     │ Track C (Drums) │
   │ Pitch/Slide/Acc │     │ Pitch/Slide/Acc │     │ BD/SD/Hat Mix   │
   └────────┬────────┘     └────────┬────────┘     └────────┬────────┘
            │                       │                       │
            └───────────────────────┼───────────────────────┘
                                    ▼
                       ┌─────────────────────────┐
                       │   Vintage Low-Pass      │
                       │   BPM-Synced Delay      │
                       └────────────┬────────────┘
                                    ▼
                       ┌─────────────────────────┐
                       │     Hardware Output     │
                       │  (Local Web Audio Node) │
                       └─────────────────────────┘
