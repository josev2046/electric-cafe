# Integrated synth workstation 

## Overview
This document outlines the signal architecture, MIDI synchronisation, and physical cabling requirements of a unified synth rig comprising the Arturia MiniBrute Mk1, Behringer TD-3-MO-AM, and Korg MS2000BR.

The configuration leverages a **serial audio path** and a **daisy-chain MIDI topology** to ensure total interconnectivity, allowing for advanced filtering and temporal processing across all units. This setup provides a robust, "DAWless" workflow focused on high-fidelity analogue signal preservation and unique sound design possibilities.

---

## 1. Signal architecture

### A. Control path (MIDI synchronisation)
To maintain rhythmic integrity across sequencers and arpeggiators, the Arturia MiniBrute Mk1 serves as the master clock.

* **Master (Arturia MiniBrute Mk1):** Generates the internal clock and transmits note data. The arpeggiator must be active to transmit MIDI clock pulses.
    * *Connection:* MIDI OUT → Korg MIDI IN.
* **Slave 1 (Korg MS2000BR):** Synchronises internal LFOs and delays to the master clock. Receives note data on MIDI channel 1.
    * *Connection:* MIDI THRU → Behringer MIDI IN.
* **Slave 2 (Behringer TD-3-MO-AM):** Synchronises the internal acid sequencer to the master clock. Set to MIDI channel 2 to ignore external note data from the MiniBrute keyboard.

### B. Audio path (serial processing)
The audio is routed serially to allow the final stage (Korg MS2000BR) to apply stereo effects to the combined output of the previous analogue stages.

1.  **Stage 1:** The **Behringer TD-3-MO-AM** generates raw acid bass and feeds into the **Arturia MiniBrute Mk1** external audio input.
2.  **Stage 2:** The MiniBrute shapes the combined signal through its Steiner-Parker filter and Brute factor overdrive.
3.  **Stage 3:** The composite mono signal is routed from the MiniBrute output into the **Korg MS2000BR** audio in 1 for effects processing and vocoding.
4.  **Stage 4:** The Korg applies stereo DSP effects and outputs a line-level stereo signal to the **Yamaha MG06X** mixer for final output control.

---

## 2. Cabling inventory

| Quantity | Item | Specification | Purpose |
| :--- | :--- | :--- | :--- |
| 2 | MIDI cable | 5-pin DIN (2m) | System synchronisation |
| 2 | Mono patch cable | 1/4" TS mono (0.6m – 0.9m) | Inter-unit audio linking |
| 2 | Instrument cable | 1/4" TS mono (1.5m – 3.0m) | Master stereo out to mixer |
| 1 | Power strip | Surge protected (6-way) | Centralised power distribution |

---

## 3. Configuration & calibration

### Arturia MiniBrute Mk1 settings
* **Gate source:** Set to 'Hold' (rear panel) to allow the TD-3 audio to pass through the filter without active key-triggering.
* **Arpeg/Free:** Set to 'Arpeg' to engage the master clock.
* **Mixer section:** Raise the 'Ext in' fader to approximately 50–60%. The Mk1 input is highly sensitive; avoid 100% to prevent unwanted clipping before the filter.

### Behringer TD-3-MO-AM settings
* **Clock source:** Set to 'MIDI' (hold BACK + WRITE/NEXT, press step 2).
* **MIDI channel:** Set to channel 2 to operate independently of the MiniBrute keyboard.

### Korg MS2000BR settings
* **Clock:** Set to 'External' in the global menu.
* **Input gain:** Adjust the 'Audio in 1' trim to ensure a clean signal level for the DSP effects engine.
* **Routing:** Utilise 'Audio in' as the modulator for vocoder patches or as a source for the internal FX bus.

---

## 4. Hardware connectivity diagram

<img width="811" height="626" alt="image" src="https://github.com/user-attachments/assets/a06082b4-9d0f-4fae-8d13-47b4b34ab40b" />


