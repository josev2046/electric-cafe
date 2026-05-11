# JV's integrated synth workstation

## Overview
This document outlines the signal architecture, MIDI synchronisation, and physical cabling requirements of my unified synth rig comprising the Arturia MiniBrute, Behringer TD-3-MO-AM, and a Korg MS2000BR.

The configuration leverages a **serial audio path** and a **daisy-chain MIDI topology** to ensure total interconnectivity, allowing for advanced filtering and temporal processing across all units.

This configuration provides a robust, "DAWless" workflow focused on high-fidelity analog signal preservation. The serial routing allows for unique sound design possibilities that traditional parallel mixing cannot achieve.

---

## 1. Signal architecture

### A. Control path (MIDI synchronisation)
To maintain rhythmic integrity across sequencers and arpeggiators, the Arturia MiniBrute serves as the master clock.

* **Master (Arturia MiniBrute):** Generates the internal clock and transmits note data.
    * *Connection:* MIDI OUT to Korg MIDI IN.
* **Slave 1 (Korg MS2000BR):** Synchronises internal LFOs and delays to the master clock. Receives note data on MIDI channel 1.
    * *Connection:* MIDI THRU to Behringer MIDI IN.
* **Slave 2 (Behringer TD-3-MO-AM):** Synchronises the internal acid sequencer to the master clock. Set to MIDI channel 2 to ignore external note data.

### B. Audio path (serial processing)
The audio is routed serially to allow the final stage (Korg MS2000BR) to apply stereo effects to the combined output of the previous analog stages.

1.  **Stage 1:** The **Behringer TD-3-MO-AM** output is routed into the **Arturia MiniBrute** external audio input.
2.  **Stage 2:** The **Arturia MiniBrute** processes the combined signal through its Steiner-Parker filter and Brute Factor overdrive.
3.  **Stage 3:** The composite mono signal is routed from the MiniBrute output into the **Korg MS2000BR** audio in 1.
4.  **Stage 4:** The Korg applies stereo DSP effects and outputs a professional line-level stereo signal to the **Yamaha MG06X** professional compact mixer.

---

## 2. Cabling inventory

| Quantity | Item | Specification | Purpose |
| :--- | :--- | :--- | :--- |
| 2 | MIDI cable | 5-pin DIN (2m) | System synchronisation |
| 2 | Mono patch cable | 1/4" TS mono (0.6m - 0.9m) | Inter-unit audio linking |
| 2 | Instrument cable | 1/4" TS mono (1.5m - 3.0m) | Master stereo out to mixer |
| 1 | Power strip | Surge protected (6-way) | Centralised power distribution |

---

## 3. Configuration & calibration

### Arturia MiniBrute settings
* **Gate source:** Set to 'Hold' or 'Audio' (rear panel) to allow external audio throughput without active key-triggering.
* **Mixer section:** Raise the 'Ext In' fader to approximately 70% to integrate the TD-3 signal without clipping the pre-amp.

### Behringer TD-3-MO-AM settings
* **Clock source:** Set to 'MIDI' (hold BACK + WRITE/NEXT, press step 2).
* **MIDI channel:** Set to channel 2 to operate independently of the MiniBrute keyboard.

### Korg MS2000BR settings
* **Clock:** Set to 'External' in the global menu.
* **Input gain:** Adjust the 'Audio In 1' trim to ensure a clean signal level for the DSP effects engine.
* **Routing:** Utilise 'Audio In' as the modulator for vocoder patches or as a source for the internal FX bus.

---

## 4. Hardware connectivity diagram
<img width="795" height="611" alt="image" src="https://github.com/user-attachments/assets/835a311a-49c8-4345-9e98-59613e9d928a" />

