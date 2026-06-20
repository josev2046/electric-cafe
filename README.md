# SQ-2046 Programmable Analog Sequencer

The SQ-2046 is a browser-based, three-track step sequencer and groovebox inspired by classic vintage hardware workflows. It combines a highly customisable scheduling engine with an authentic sound signature, serving as a powerful standalone virtual instrument.

---

## Technical Capabilities

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
                       │   Internal Audio Out    │
                       │  (Local Web Audio Node) │
                       └─────────────────────────┘
```

---

## High-Level Operation

### 1. Standalone Synthesis
*   **Clock Configuration:** Set the global tempo slider (80–180 BPM) and select a playback vector (Forward, Reverse, Ping-Pong, Random).
*   **Step Sequencing:** Input raw numerical offsets for pitch intervals on the grid, map step-specific filter parameters via the vertical faders, and engage the `[ S ]` or `[ A ]` modifiers to dial in rhythmic variation.
*   **Key Offsets:** Transpose the entire sequence in real time using the integrated 12-key chromatic pitch interface.

### 2. Live Deployment (Offline Environments)
*   **Offline Execution:** The application evaluates audio entirely on the client-side device using the browser's built-in processing loops. When assets are stored locally, it does not require active server communication to generate sound or run the logic arrays, making it robust for live performance.

---

## Development Roadmap

*   **Web MIDI Integration:** Future updates will include external MIDI routing, allowing the SQ-2046 to act as a master brain for external hardware synths (e.g., sending slide/accent velocity data to external CV filters).
*   **Local Off Mode:** The ability to decouple the internal Web Audio engines to function purely as a sequence controller.
*   **External Clock Sync:** Slaving the sequencer to an external DAW transport.

---

## License & Copyright

**Copyright (c) 2046 Jose Velazquez**

This software is released under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
