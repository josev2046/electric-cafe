
# KORG MS2000 PATCH SHEET: "EUROPE ENDLESS" GROOVEBOX

**Concept:** A 1-key split patch. The lowest key triggers an automated, 16-step "Motorik" analog drum loop. The upper keys trigger an arpeggiated, bouncing square-wave melody with a 16-step automated filter sweep.

## 1. GLOBAL SETUP & KEYBOARD SPLIT
Start from an **Initialized Patch**.
1. Press the **SPLIT** button so it is lit.
2. Turn the **TEMPO** knob to `120`.
3. Press the **EDIT** button. Page to `03: Common`.
4. Set **SplitPoint:** `C#2`. *(Key C2 and below triggers drums. C#2 and above triggers melody).*
5. Press **EDIT** to exit.
6. Press **ARP ON/OFF** so it is lit. Press **LATCH** so it is lit. 
7. Set Arp Target to **Timbre 1**. Set Arp Type to `UP`.

---

## 2. TIMBRE 1: MOTORIK DRUMS (LEFT HAND)
Press **TIMBRE SELECT** until **TIMBRE 1** is lit green.

### A. Sound Shaping
*   **OSC 1:** Waveform = `TRIANGLE`. 
*   **Mixer:** OSC 1 Level = `127` (Max). OSC 2 Level = `0`. Noise Level = `0`.
*   **Filter:** Type = `24dB LPF`. Cutoff = `9 o'clock`. Resonance = `12 o'clock`.
*   **EG2 (Amp):** Attack = `0`, Decay = `0`, Sustain = `127` (Max), Release = `0`.
*   **Amp Page:** Pan = `L63` (Hard Left - *optional for external mixing*).

### B. Mod Sequencer Routing
Ensure **MOD SEQ ON/OFF** is lit. Press **EDIT**.
*   **Track 1 (Kick/Snare Body):** Dest = `Cutoff` | Motion = `Step` | Length = `16`
*   **Track 2 (Hat/Snare Sizzle):** Dest = `Noise Level` | Motion = `Step` | Length = `16`
*   **Track 3:** Unassigned.

### C. Drum Sequencer Values
*Hold step buttons 1-16 and turn the VALUE dial to enter these values.*

| Step | Hit | Trk 1 (Cutoff) | Trk 2 (Noise) | | Step | Hit | Trk 1 (Cutoff) | Trk 2 (Noise) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | **Kick** | `+00` | `+00` | | **9** | **Kick** | `+00` | `+00` |
| **2** | Hat | `+15` | `+25` | | **10** | Hat | `+15` | `+25` |
| **3** | Hat | `+15` | `+25` | | **11** | Hat | `+15` | `+25` |
| **4** | Hat | `+15` | `+25` | | **12** | Hat | `+15` | `+25` |
| **5** | **Snare**| `+40` | `+63` | | **13** | **Snare**| `+40` | `+63` |
| **6** | Hat | `+15` | `+25` | | **14** | Hat | `+15` | `+25` |
| **7** | Hat | `+15` | `+25` | | **15** | Hat | `+15` | `+25` |
| **8** | Hat | `+15` | `+25` | | **16** | Hat | `+15` | `+25` |

---

## 3. TIMBRE 2: BOUNCING MELODY (RIGHT HAND)
Press **TIMBRE SELECT** until **TIMBRE 2** is lit green.

### A. Sound Shaping
*   **OSC 1:** Waveform = `SQUARE`.
*   **Filter:** Type = `24dB LPF`. Cutoff = `8 o'clock`. EG1 Intensity = `2 o'clock`.
*   **EG1 (Filter):** Attack = `0`, Decay = `10 o'clock`, Sustain = `0`, Release = `0`.
*   **EG2 (Amp):** Attack = `0`, Decay = `10 o'clock`, Sustain = `0`, Release = `0`.
*   **Amp Page:** Pan = `R63` (Hard Right - *optional for external mixing*).

### B. Mod Sequencer Routing
Ensure **MOD SEQ ON/OFF** is lit. Press **EDIT**.
*   **Track 1 (Octave Bounces):** Dest = `Pitch` | Motion = `Step` | Length = `16`
*   **Track 2 (Slow Filter Sweep):** Dest = `Cutoff` | Motion = `Smooth` | Length = `16`
*   **Track 3:** Unassigned.

### C. Melody Sequencer Values
*Hold step buttons 1-16 and turn the VALUE dial to enter these values.*

| Step | Trk 1 (Pitch) | Trk 2 (Sweep) | | Step | Trk 1 (Pitch) | Trk 2 (Sweep) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | `+00` | `+00` | | **9** | `+00` | `+40` (Peak) |
| **2** | `+00` | `+05` | | **10** | `+00` | `+35` |
| **3** | `+12` (Octave)| `+10` | | **11** | `+12` (Octave)| `+30` |
| **4** | `+00` | `+15` | | **12** | `+00` | `+25` |
| **5** | `+00` | `+20` | | **13** | `+00` | `+20` |
| **6** | `+12` (Octave)| `+25` | | **14** | `+12` (Octave)| `+15` |
| **7** | `+00` | `+30` | | **15** | `+00` | `+10` |
| **8** | `+00` | `+35` | | **16** | `+12` (Octave)| `+05` |

---

## 4. SAVE & PERFORM
1. Press **WRITE** twice immediately to save the patch to memory.
2. **To Play:** Tap the lowest `C2` key on the keyboard. The arpeggiator will latch, and the drum machine will loop continuously.
3. Play any single key above `C#2` with your right hand to trigger the automated 16-step melody sequence. Move your right finger to transpose the melody live.


