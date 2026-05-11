# JV's Integrated Synth Workstation

## Overview
This document outlines the signal architecture, MIDI synchronisation, and physical cabling requirements of my unified synth rig comprising the Arturia MiniBrute, Behringer TD-3-MO-AM, and a Korg MS2000BR.

The configuration leverages a **Serial Audio Path** and a **Daisy-Chain MIDI Topology** to ensure total interconnectivity, allowing for advanced filtering and temporal processing across all units.

This configuration provides a robust, "DAWless" workflow while maintaining the ability to record a polished stereo master via the USB interface. The serial routing allows for unique sound design possibilities that traditional parallel mixing cannot achieve.

---

## 1. Signal Architecture

### A. Control Path (MIDI Synchronisation)
To maintain rhythmic integrity across sequencers and arpeggiators, the Arturia MiniBrute serves as the Master Clock.

* **Master (Arturia MiniBrute):** Generates the internal clock and transmits note data.
    * *Connection:* MIDI OUT to Korg MIDI IN.
* **Slave 1 (Korg MS2000BR):** Synchronises internal LFOs and Delays to the Master Clock. Receives note data on MIDI Channel 1.
    * *Connection:* MIDI THRU to Behringer MIDI IN.
* **Slave 2 (Behringer TD-3-MO-AM):** Synchronises the internal acid sequencer to the Master Clock. Set to MIDI Channel 2 to ignore external note data.

### B. Audio Path (Serial Processing)
The audio is routed serially to allow the final stage (Korg MS2000BR) to apply stereo effects to the combined output of the previous analog stages.

1.  **Stage 1:** The **Behringer TD-3-MO-AM** output is routed into the **Arturia MiniBrute** External Audio Input.
2.  **Stage 2:** The **Arturia MiniBrute** processes the combined signal through its Steiner-Parker filter and Brute Factor overdrive.
3.  **Stage 4:** The composite mono signal is routed from the MiniBrute output into the **Korg MS2000BR** Audio In 1.
4.  **Stage 5:** The Korg applies stereo DSP effects (Delay, Chorus, Flanger) and outputs a professional line-level stereo signal to the **Behringer XENYX QX1204USB** mixer.

---

## 2. Professional Cabling Inventory

| Quantity | Item | Specification | Purpose |
| :--- | :--- | :--- | :--- |
| 2 | MIDI Cable | 5-Pin DIN (2m) | System Synchronisation |
| 2 | Mono Patch Cable | 1/4" TS Mono (0.6m - 0.9m) | Inter-unit Audio Linking |
| 2 | Instrument Cable | 1/4" TS Mono (1.5m - 3.0m) | Master Stereo Out to Mixer |
| 1 | USB Cable | Type-A to Type-B | Mixer to PC/Mac Recording |
| 1 | Power Strip | Surge Protected (6-Way) | Centralised Power Distribution |

---

## 3. Configuration & Calibration

### Arturia MiniBrute Settings
* **Gate Source:** Set to 'Hold' or 'Audio' (rear panel) to allow external audio throughput without active key-triggering.
* **Mixer Section:** Raise the 'Ext In' fader to approximately 70% to integrate the TD-3 signal without clipping the pre-amp.

### Behringer TD-3-MO-AM Settings
* **Clock Source:** Set to 'MIDI' (Hold BACK + WRITE/NEXT, press Step 2).
* **MIDI Channel:** Set to Channel 2 to operate independently of the MiniBrute keyboard.

### Korg MS2000BR Settings
* **Clock:** Set to 'External' in the Global Menu.
* **Input Gain:** Adjust the 'Audio In 1' trim to ensure a clean signal level for the DSP effects engine.
* **Routing:** Utilise 'Audio In' as the Modulator for Vocoder patches or as a source for the internal FX bus.

---

## 4. Hardware Connectivity Diagram
<img width="755" height="612" alt="image" src="https://github.com/user-attachments/assets/45a5eb12-6b8e-44c3-8c03-1a3286848a86" />




