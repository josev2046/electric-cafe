# Suicide - "Ghost rider" 

Operational steps to perform "Ghost rider" using a serial signal path. The **Arturia MiniBrute** serves as the master clock and keyboard, the **Behringer TD-3-MO** provides the hypnotic bass, and the **Korg MS2000BR** handles the lead textures.

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
* **MiniBrute:** Set the rear **GATE SOURCE** switch to **HOLD**. On the front mixer, set **Audio in** to 100% and all internal oscillators to 0%.
* **TD-3-MO:** Set clock to **MIDI** (Hold `BACK` + `WRITE/NEXT`, then press `Step 2`). Ensure it is on MIDI Channel 2.
* **Korg MS2000BR:** Set **Global MIDI** to **Channel 1**. Set **Clock** to **External**.

### Step 2: Program the bass pulse (TD-3-MO)
1.  **Clear:** Press `FUNCTION` + `PATTERN CLEAR`.
2.  **Pitch:** Press `PITCH MODE`. Tap the **C key** 16 times.
3.  **Time:** Press `TIME MODE`. Tap the **Note button** 16 times.
4.  **Test:** Press `RUN`. You should hear a steady, dark "donk-donk" pulse.

### Step 3: Sculpt the grime (MiniBrute)
1.  **Cutoff:** Set to 20% (Muffled).
2.  **Resonance:** Set to 20%.
3.  **Brute factor:** Set to 50%. This adds the essential NYC grit.

### Step 4: Prepare the void (Korg)
1.  **Patch:** Select a thin organ or sine lead.
2.  **Delay:** Set to a "slapback" (short time, 2–3 repeats).

---

## 3. The performance routine

### 0:00–0:30 – The intro
* Press **RUN** on the TD-3.
* Slowly turn the MiniBrute **Cutoff** from 20% to 60%. Imagine the sound emerging from a dark tunnel.

### 0:30–1:00 – The lead hook
* Using the MiniBrute keys, play the eerie G–E cycle:
    * **G** (High octave): Hold for 2 beats.
    * **E**: Hold for 2 beats.
* The Korg will provide the melody; the MiniBrute provides the grit.

### 1:00–1:30 – The tension
* Continue the G–E melody with your right hand.
* With your left hand, slowly sweep the MiniBrute **Resonance** up to 80% and back to 20%. This makes the bass "scream" and recede.

### 1:30–Finish – The climax
* **Option A:** If using a mic, perform breathless, Alan Vega-style vocals.
* **Option B:** Crank the **Brute factor** to 100% for 4 bars, then return to 50%.
* **Resolution:** Abruptly turn **Cutoff** to 0% and stop the TD-3.

---

## 4. Troubleshooting
* **No sync:** Check that TD-3 is definitely in MIDI clock mode, not Internal.
* **No audio:** Ensure the MiniBrute **Gate source** is on **HOLD**; otherwise, the TD-3 audio is blocked until you hit a key.
* **Distortion too high:** Back off the **Brute factor**. It is a powerful feedback loop that can quickly overwhelm the mix.
