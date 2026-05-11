# Suicide - "Ghost rider" 

Operational steps to perform "Ghost rider" using a serial signal path. The **Arturia MiniBrute Mk1** serves as the master clock and keyboard, the **Behringer TD-3-MO** provides the hypnotic bass, and the **Korg MS2000BR** handles the lead textures.

---

## 1. Pre-performance setup

### Audio & MIDI routing verification
1.  **MIDI cables:**
    * MiniBrute MIDI OUT → Korg MIDI IN
    * Korg MIDI THRU → TD-3 MIDI IN
2.  **Audio cables:**
    * TD-3 LINE OUT → MiniBrute AUDIO IN (Rear)
    * MiniBrute LINE OUT → Korg AUDIO IN 1 (Rear)
    * Korg STEREO OUT (L/R) → Yamaha MG06X Line 3/4
3.  **Power sequence:**
    * 1. Yamaha Mixer | 2. MiniBrute | 3. TD-3 | 4. Korg

---

## 2. Step-by-step configuration

### Step 1: Synchronise the instruments
* **MiniBrute Mk1:** Set the rear **GATE SOURCE** switch to **HOLD**. Set the **Arpeg/Free** switch to **Arpeg** (essential for master clock). In the mixer section, set **Audio in** to **60%** and all internal oscillators to 0%.
* **TD-3-MO:** Set clock to **MIDI** (Hold `BACK` + `WRITE/NEXT`, then press `Step 2`). Ensure it is on MIDI Channel 2.
* **Korg MS2000BR:** Set **Global MIDI** to **Channel 1**. Set **Clock** to **External**.

### Step 2: Program the bass pulse (TD-3-MO)
1.  **Clear:** Press `FUNCTION` + `PATTERN CLEAR`.
2.  **Pitch:** Press `PITCH MODE`. Tap the **C key** 16 times.
3.  **Time:** Press `TIME MODE`. Tap the **Note button** 16 times.
4.  **Test:** Press `RUN`. You should hear a steady, dark "donk-donk" pulse.

### Step 3: Sculpt the grime (MiniBrute Mk1)
1.  **Cutoff:** Set to 20% (Muffled).
2.  **Resonance:** Set to 20%.
3.  **Brute factor:** Set to 50%. This adds the essential NYC grit without losing the bass fundamental.

### Step 4: Prepare the void (Korg)
1.  **Patch:** Select a thin organ or sine lead.
2.  **Delay:** Set to a "slapback" (short time, 2–3 repeats).

---

## 3. The performance routine

### 0:00–0:30 – The intro
* Press **RUN** on the TD-3.
* Slowly turn the MiniBrute **Cutoff** knob from 20% to 60%. Imagine the sound emerging from a dark tunnel.

### 0:30–1:00 – The lead hook
* Using the MiniBrute keys, play the eerie G–E cycle:
    * **G** (High octave): Hold for 2 beats.
    * **E**: Hold for 2 beats.
* The Korg will provide the melody; the MiniBrute filter provides the grit.

### 1:00–1:30 – The tension
* Continue the G–E melody with your right hand.
* With your left hand, slowly sweep the MiniBrute **Resonance** up to 80% and back to 20%. This makes the bass "scream" and recede.

### 1:30–Finish – The climax
* **Option A:** If using a mic, perform breathless, Alan Vega-style vocals.
* **Option B:** Crank the **Brute factor** to 100% for 4 bars, then return to 50%.
* **Resolution:** Abruptly turn **Cutoff** to 0% and stop the TD-3.

---

## 4. Troubleshooting
* **No sync:** Ensure the MiniBrute Mk1 is in **Arpeg** mode; it will not send MIDI clock in 'Free' mode.
* **No audio:** Verify the rear **Gate source** is on **HOLD**.
* **Audio is too distorted:** Lower the **Audio in** fader on the MiniBrute mixer; the Mk1 input is very sensitive to line-level signals.
