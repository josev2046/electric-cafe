# KORG MS2000 PATCH SHEET: "THE MAN-MACHINE" GROOVEBOX

**Concept:** A heavy, slow, industrial 1-key split. The drums feature a syncopated, mechanical strut. The bassline is an aggressive, squelchy sawtooth pattern in a minor key, with the filter heavily accented on the octave jumps to make the synthesizer "talk."

## 1. GLOBAL SETUP & KEYBOARD SPLIT
Start from an **Initialized Patch**.
1. Press the **SPLIT** button so it is lit.
2. Turn the **TEMPO** knob to `110` (Slower, heavier tempo).
3. Press the **EDIT** button. Page to `03: Common`.
4. Set **SplitPoint:** `C#2`. 
5. Press **EDIT** to exit.
6. Press **ARP ON/OFF** so it is lit. Press **LATCH** so it is lit. 
7. Set Arp Target to **Timbre 1**. Set Arp Type to `UP`.

---

## 2. TIMBRE 1: INDUSTRIAL DRUMS (LEFT HAND)
Press **TIMBRE SELECT** until **TIMBRE 1** is lit green.

### A. Sound Shaping
*   **OSC 1:** Waveform = `TRIANGLE`. (Drop it down 1 octave using the physical Pitch/Transpose buttons if needed for a deeper sub).
*   **Mixer:** OSC 1 Level = `127` (Max). OSC 2 Level = `0`. Noise Level = `0`.
*   **Filter:** Type = `24dB LPF`. Cutoff = `9 o'clock`. Resonance = `1 o'clock` (Slightly higher for a more metallic thud).
*   **EG2 (Amp):** Attack = `0`, Decay = `0`, Sustain = `127` (Max), Release = `0`.

### B. Mod Sequencer Routing
Ensure **MOD SEQ ON/OFF** is lit. Press **EDIT**.
*   **Track 1 (Kick/Snare Body):** Dest = `Cutoff` | Motion = `Step` | Length = `16`
*   **Track 2 (Hat/Snare Sizzle):** Dest = `Noise Level` | Motion = `Step` | Length = `16`

### C. Drum Sequencer Values
*Note the syncopated Kick drum on Step 7 to give it that heavy mechanical strut.*

| Step | Hit | Trk 1 (Cutoff) | Trk 2 (Noise) | | Step | Hit | Trk 1 (Cutoff) | Trk 2 (Noise) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | **Kick** | `+00` | `+00` | | **9** | **Kick** | `+00` | `+00` |
| **2** | Hat | `+15` | `+25` | | **10** | Hat | `+15` | `+25` |
| **3** | Hat | `+15` | `+25` | | **11** | Hat | `+15` | `+25` |
| **4** | Hat | `+15` | `+25` | | **12** | Hat | `+15` | `+25` |
| **5** | **Snare**| `+40` | `+63` | | **13** | **Snare**| `+40` | `+63` |
| **6** | Hat | `+15` | `+25` | | **14** | Hat | `+15` | `+25` |
| **7** | **Kick** | `+00` | `+00` | | **15** | Hat | `+15` | `+25` |
| **8** | Hat | `+15` | `+25` | | **16** | Hat | `+15` | `+25` |

---

## 3. TIMBRE 2: SQUELCHY MACHINE BASS (RIGHT HAND)
Press **TIMBRE SELECT** until **TIMBRE 2** is lit green.

### A. Sound Shaping
*   **OSC 1:** Waveform = `SAW`.
*   **OSC 2:** Waveform = `SAW`. Tune = `0`. Fine = `+6` (Slight detune for thickness).
*   **Filter:** Type = `24dB LPF`. Cutoff = `8 o'clock`. Resonance = `2 o'clock` (High resonance for squelch). EG1 Intensity = `2 o'clock`.
*   **EG1 (Filter):** Attack = `0`, Decay = `9 o'clock` (Very fast snap), Sustain = `0`, Release = `0`.
*   **EG2 (Amp):** Attack = `0`, Decay = `11 o'clock` (Slightly longer than the filter), Sustain = `0`, Release = `0`.

### B. Mod Sequencer Routing
Ensure **MOD SEQ ON/OFF** is lit. Press **EDIT**.
*   **Track 1 (Minor Key Melody):** Dest = `Pitch` | Motion = `Step` | Length = `16`
*   **Track 2 (Acid Filter Accents):** Dest = `Cutoff` | Motion = `Step` | Length = `16`

### C. Melody Sequencer Values
*This sequence uses a minor 3rd (+3) and a perfect fifth (+7). Track 2 spikes the filter open hard on the off-beats.*

| Step | Trk 1 (Pitch) | Trk 2 (Accent) | | Step | Trk 1 (Pitch) | Trk 2 (Accent) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | `+00` (Root) | `+00` | | **9** | `+00` (Root) | `+00` |
| **2** | `+00` (Root) | `+00` | | **10** | `+00` (Root) | `+00` |
| **3** | `+12` (Octave)| `+20` (Pop!) | | **11** | `+07` (Fifth) | `+30` (Big Pop!)|
| **4** | `+00` (Root) | `+00` | | **12** | `+00` (Root) | `+00` |
| **5** | `+03` (Min 3rd)| `+30` (Big Pop!)| | **13** | `+12` (Octave)| `+20` (Pop!) |
| **6** | `+00` (Root) | `+00` | | **14** | `+00` (Root) | `+00` |
| **7** | `+12` (Octave)| `+20` (Pop!) | | **15** | `+03` (Min 3rd)| `+30` (Big Pop!)|
| **8** | `+00` (Root) | `+00` | | **16** | `+00` (Root) | `+00` |

---

## 4. SAVE & PERFORM
1. Press **WRITE** twice immediately to save the patch.
2. **To Play:** Tap the lowest `E1` or `C2` key. The heavy drum machine will latch and begin grinding.
3. Play the `E` key in the right-hand zone to trigger the minor-key sequence. It will sound tight and closed on the root notes, but the high octave and minor 3rd notes will violently pop the filter open, creating that classic robotic "talking" bass effect.
