# Korg MS2000BR × Macromassa Patching Cheat Sheet

---

## 1. Audio Generator (Unstable Pitch)
*Replicate the microtonal, drifting, uncalibrated sound of Macromassa’s custom hardware.*

* **OSC 1 & 2 Detune:** Set `OSC 2 Detune` to **+5 to +15** cents. For heavy dissonance, set `OSC 2 Transpose` to **+1 or -1** semitone.
* **Pitch Drift (LFO 1):** * `Waveform`: **Triangle**
    * `Frequency (Speed)`: **Slow (0.5Hz - 1Hz)**
    * `Mod Dest`: **Pitch**
    * `Mod Depth`: **+2 to +5** (Keep it subtle; just enough to mimic a failing power supply).
* **Random Chaos (LFO 2):**
    * `Waveform`: **S&H (Sample & Hold)**
    * `Mod Dest`: **OSC 2 Pitch** or **Filter Cutoff**
    * `Mod Depth`: **+15 to +30** (Creates unpredictable stepping).

---

## 2. Industrial & Metallic Textures
*Harsh, clangorous, concrete, and non-traditional waveforms.*

| Parameter | Setting | Sonic Result |
| :--- | :--- | :--- |
| **OSC 1 Wave** | `Noise` or `Vox Wave` | Static grime or eerie formant textures. |
| **OSC 2 Wave** | `Saw` or `Square` | Core harmonic body. |
| **OSC 2 Mod** | `Ring` or `Cross` | Instantly creates metallic, bell-like, or harsh FM tones. |
| **Mixer** | `Noise` knob at **50% or higher** | Emulates vintage tape hiss and industrial static. |

---

## 3. External Processing (The Clarinet/Vocal Mutation)
*Replicate Víctor Nubla and Juan Crek’s technique of mutating acoustic woodwinds and vocals.*

* **Routing:** Plug your source (mic, woodwind, or sample) into **Input 1 (Audio)** on the back.
* **Synth Filter Setup:**
    * `OSC 1 Wave`: Select **AUDIO IN**.
    * `Filter Type`: **4-Pole LPF** (for deep growls) or **BPF** (for reedy, radio-like constraints).
    * `Resonance`: Crank to **80% - 95%** (Right to the edge of self-oscillation).
    * `Filter EG Intensity`: High positive or negative values to snap the filter open on instrument transients.

### The Avant-Garde Vocoder Setup
1. Turn the **Vocoder** switch **ON**.
2. Connect voice/woodwind to **Input 1 (Analysis)**.
3. Connect an internal synth pad or noise generator to **Input 2 (Carrier)**.
4. Adjust `Formant Shift` to morph the acoustic instrument into unnatural, synthetic registers.

---

## 4. Generative Sequencing & Gritty FX
*Non-linear arrangements and harsh sonic degradation.*

* **Mod Sequencer (The Anti-Melody Tool):**
    * Set `Seq 1` to target **Filter Cutoff** or **OSC 2 Pitch**.
    * Dial in completely random values for all 16 steps. 
    * Set `Motion` to **Smooth** for slurring, organic mutations, or **Step** for mechanical rhythmic stutter.
* **Amp Section:** Turn the `Distortion` switch **ON** to instantly compress, saturate, and anger the signal.
* **Delay Section:** * `Type`: **Stereo Delay**
    * `Feedback`: **80% - 90%** (Infinite tape loop territory).
    * *Performance Trick:* Physically twist the `Delay Time` knob back and forth while audio plays to create warping, elastic pitch-bends.
