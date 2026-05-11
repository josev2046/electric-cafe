# "Ghost Rider" 

## Pre-Performance Setup

### Audio & MIDI Routing Verification

Before anything else, verify your cables:

1. **MIDI cables:**
   - MiniBrute MIDI OUT → Korg MIDI IN (5-pin DIN connector)
   - Korg MIDI THRU → TD-3 MIDI IN (5-pin DIN connector)

2. **Audio cables:**
   - TD-3 LINE OUT (mono, 1/4" jack) → MiniBrute AUDIO IN
   - MiniBrute LINE OUT → Korg AUDIO IN 1
   - Korg STEREO OUT → Yamaha MG06X Line In 3/4
   - Yamaha MG06X MAIN OUT → speakers or monitoring system

3. **Power on in this order:**
   - Yamaha mixer first
   - MiniBrute second
   - TD-3 third
   - Korg last

### Mixer Baseline

Set the Yamaha MG06X to a known state:

- Channels 1–2: Faders to −∞ (muted)
- Line In 3/4 fader: −6 dB (you'll bring this up during performance)
- Master fader: −6 dB
- No EQ or effects on the mixer itself

**Test:** Tap the TD-3 with your finger (vibration through the mic input if present). You should hear silence from the speakers. Good.

---

## Step 1: Synchronise the Instruments (The Sync)

### MiniBrute Setup

1. Press the power button. Wait 10 seconds for full boot.
2. Locate the rear panel. Find the **GATE SOURCE** switch (usually labelled GATE, EXT, or HOLD).
3. Slide it to **HOLD**. This allows external audio to pass through without requiring you to press a key.
4. On the front panel, locate the **AUDIO IN fader** (left side, usually black/grey). Turn it fully clockwise to **100%**.
5. Locate the **INTERNAL OSCILLATORS** section (Saw, Square, Triangle switches). Set all to **OFF** (down position).
6. **MiniBrute is now in "pass-through" mode.** It will receive audio from the TD-3 and route it through the filter.

### TD-3 MIDI Configuration

1. Power on the TD-3. Wait 5 seconds.
2. Press **BACK** button on the rear panel.
3. Press **WRITE/NEXT** button immediately after (do not hold, just tap).
4. Look at the LED display. It should show something like "STEP: 1" or "PATTERN: 1."
5. Press **Step 2** on the sequencer buttons.
6. The display should now show "MIDI CLOCK: EXT" or similar. If it shows "INT," tap the **FUNCTION** button until MIDI CLOCK cycles to **EXTERNAL**.
7. **Verify:** The TD-3 is now listening for clock pulses from the MiniBrute.

### Korg MS2000BR MIDI Configuration

1. Power on the Korg. Wait 5 seconds.
2. Press the **MENU** button on the right side.
3. Scroll with the **+/−** buttons until you see "MIDI CHANNEL" or "GLOBAL CHANNEL."
4. Use the **VALUE** dial to set it to **CHANNEL 1**.
5. Press **MENU** again to exit.
6. **Verify:** The Korg is now listening for MIDI note messages on Channel 1.

**Checkpoint:** All three instruments are powered and configured. Move to Step 2.

---

## Step 2: Program the TD-3 Bass Sequence

The TD-3 will play a repetitive 16-step bass line. Every note will be C (the root), creating a hypnotic pulse.

### Clear the Current Pattern

1. Press **FUNCTION** button.
2. Press **PATTERN CLEAR** (usually labelled with a trash/delete icon on the interface).
3. The LED should flash. Wait 2 seconds.
4. Press **FUNCTION** again to confirm and exit.

### Enter the 16 Notes (All C)

1. Press the **PITCH MODE** button (usually a keyboard or note icon).
2. Locate the sequencer keyboard at the bottom of the unit. It has keys labelled C, D, E, F, etc.
3. **Tap the C key (lowest note on the keyboard) exactly 16 times.** Do not hold; tap once per beat. Count aloud: "One, two, three..." to keep pace.
4. After the 16th tap, the LED should show "STEP: 16" or loop back to "STEP: 1."

### Set the Timing (Rhythm)

1. Press **TIME MODE** button.
2. Locate the **NOTE button** (usually marked with a note symbol, next to the TIE button).
3. **Tap the NOTE button 16 times.** This sets each step to play for one beat.
4. Count aloud again to ensure you hit exactly 16 taps.

### Finalise and Test

1. Press **RUN** button (usually a play symbol ▶).
2. **Listen carefully.** You should hear a repeating "donk-donk-donk-donk" sound from the TD-3 itself, with no pitch variation.
3. The tempo should feel like a steady heartbeat. If it sounds erratic, go back to PATTERN CLEAR and try again.

**Checkpoint:** The TD-3 is playing a steady 16-step pulse. Continue.

---

## Step 3: Configure the MiniBrute Filter (Sculpt the Grime)

The TD-3 bass is now flowing through the MiniBrute's Steiner-Parker filter. You'll use the filter to shape the tone.

### Filter Baseline Settings

Locate these controls on the MiniBrute front panel:

1. **Cutoff knob** (usually central, marked 0–100% or a frequency range). Turn it to **20%** (fully counter-clockwise or nearly so).
2. **Resonance knob** (to the right of Cutoff, marked 0–100%). Turn it to **20%**.
3. **Brute Factor knob** (marked ENV AMT or similar). Set it to **50%** (midway).

### Verify Pass-Through

1. You should now hear the TD-3 bass coming through the MiniBrute, heavily muffled and dark.
2. If you hear nothing, check:
   - Audio IN fader on MiniBrute is at 100%.
   - TD-3 LINE OUT cable is firmly seated.
   - Yamaha mixer's Line In 3/4 fader is not at −∞.

**Checkpoint:** The TD-3 bass is running through the MiniBrute filter. The sound is dark and muffled.

---

## Step 4: Prepare the Korg MS2000BR (The Lead Texture)

The Korg will play high, eerie synth notes triggered by your keyboard playing on the MiniBrute.

### Select a Patch

1. Press **PATCH** button on the Korg.
2. Use **+/−** buttons to browse patches. Look for:
   - "Organ" or "Electric Piano" (thin, slightly retro)
   - "Sine Lead" or "High Sine" (pure, hollow tone)
   - Avoid lush pads or reverb-heavy presets.
3. Press **PATCH** again to confirm your choice.

### Set Up Delay Effect

1. Press **FX** or **EFFECTS** button.
2. Scroll until you see "DELAY" or "ECHO."
3. Set **Delay Time** to approximately **0.5 seconds** (500 ms).
4. Set **Delay Repeats** to **2–3** (not infinite).
5. Set **Delay Level** to **40%** (audible but not overwhelming).
6. Press **FX** again to exit.

**Checkpoint:** The Korg is loaded with a thin, eerie synth patch and a slapback delay effect.

---

## Step 5: The Live Performance (The Routine)

You are now ready to perform "Ghost Rider." This is a **live, real-time performance**, not a playback. You must conduct it with your hands.

### 0:00–0:30 Seconds – The Intro

**What you do:**

1. Press **RUN** on the TD-3 to start the sequencer.
2. **Listen.** The bass pulse should be steady, dark, and muffled.
3. With your **right hand**, slowly turn the MiniBrute **Cutoff knob** from **20% to 60%** over the course of 30 seconds. Go slowly—imagine you're opening a door very gradually.
4. **As the cutoff opens**, the bass becomes brighter and more distorted. This is the "Ghost Rider" grit emerging.
5. **Your left hand does nothing during this section.** Just listen and turn the knob.

**What you're listening for:**
- The bass transitions from a muffled thud to a slightly nasal, gritty tone.
- No sudden jumps or glitches.
- Steady rhythm throughout.

### 0:30–1:00 Seconds – The Lead Hook

**What you do:**

1. **With your right hand**, play the MiniBrute keyboard. Play these two notes repeatedly:
   - **G** (one octave above middle C): Hold for **2 beats** (approximately 1 second at 124 BPM).
   - **E** (two keys to the right of G): Hold for **2 beats**.
   - Repeat this G–E–G–E cycle.

2. **Why this works:** The MiniBrute sends MIDI note data to the Korg. When you press G, the Korg plays its synth patch at the G pitch. When you press E, it plays at E. The Korg's delay effect adds a "slapback" echo, creating a haunting, repetitive melody.

3. **Your left hand does nothing yet.**

**What you're listening for:**
- The G and E notes trigger eerie, hollow tones from the Korg.
- The delay creates repeating echoes that fade.
- The bass continues its steady pulse underneath.
- The overall sound feels hypnotic and repetitive.

### 1:00–1:30 Seconds – The Tension

**What you do:**

1. **Your right hand continues** playing the G and E notes (G for 2 beats, E for 2 beats, repeat).
2. **Your left hand now manipulates the MiniBrute Resonance knob:**
   - Start at 20% (current position).
   - Over 30 seconds, slowly sweep it up to **80%**.
   - Then sweep it back down to **20%**.
   - Repeat this up-and-down sweep 2–3 times.

3. **Why this works:** High resonance causes the filter to "ring" or "scream." Combined with the cutoff setting, this creates intense feedback tones that build tension.

**What you're listening for:**
- The bass develops a "screaming" overtone as resonance increases.
- When resonance is at 80%, the bass sounds aggressive and almost threatening.
- When you drop it back to 20%, there's a sense of relief.
- The G–E melody continues underneath, hypnotic and eerie.

### 1:30–Finish – The Climax & Resolution

**Option A: Vocal Performance (if you have a microphone connected to the Korg)**

1. Keep playing G and E on the MiniBrute keyboard (right hand).
2. Keep sweeping resonance (left hand).
3. Perform a breathy, gasping vocal into the Korg microphone input. Alan Vega-style vocals are thin, breathless, and raw. Think panic or desperation.
4. Let the vocal sit high in the mix—it should feel exposed and vulnerable.

**Option B: Instrumental Climax (if no microphone)**

1. Keep playing G and E on the MiniBrute keyboard (right hand).
2. **With your left hand, turn the MiniBrute Brute Factor knob to 100%** (fully clockwise).
3. Hold it there for **4 bars** (approximately 8 seconds at 124 BPM).
4. This creates an "audio explosion"—maximum distortion and feedback.
5. After 4 bars, turn the Brute Factor back down to **50%**.

### The Finish (Both Options)

1. **Abruptly turn the MiniBrute Cutoff knob to 0%** (fully counter-clockwise). This kills the bass instantly.
2. Stop playing the MiniBrute keyboard (your right hand).
3. Press **STOP** on the TD-3.
4. Silence. Hold for 2 seconds.
5. Fade the Yamaha mixer's Line In 3/4 fader down to −∞ to prevent any residual noise.

**What you're listening for:**
- A dramatic cut to silence.
- No lingering notes or feedback.
- The performance ends cleanly and intentionally.

---

## Troubleshooting

| Problem | Cause | Solution |
|---------|-------|----------|
| No sound from TD-3 at all | MIDI clock not syncing | Verify TD-3's clock source is set to EXTERNAL, not INTERNAL. Restart both MiniBrute and TD-3. |
| TD-3 sounds wrong or not a steady pulse | Sequencer programmed incorrectly | Go back to Step 2. Press PATTERN CLEAR and reprogram all 16 steps as C notes. |
| Korg doesn't respond to keyboard | MIDI channel mismatch | Verify Korg's MIDI channel is set to 1 and MiniBrute MIDI OUT is sending on Channel 1. |
| Bass sounds thin or disappears when I open the filter | Resonance too high causing self-oscillation | Lower the Resonance knob to 30%. Try again. |
| Feedback/screaming is uncontrollable | Resonance and Brute Factor both too high | Turn Resonance down to 20% and Brute Factor to 30%. Adjust gradually during performance. |
| No sound from the mixer | Fader at −∞ | Check Yamaha's Line In 3/4 fader. Bring it to −3 dB minimum. |

---

## Performance Timing Reference

- **Intro (30 sec):** Slow cutoff sweep. No keyboard playing.
- **Lead (30 sec):** G–E–G–E on keyboard. Cutoff stays at 60%.
- **Tension (30 sec):** Resonance sweeps. G–E continues.
- **Climax (15–30 sec):** Vocal or Brute Factor explosion. High intensity.
- **Finish (5 sec):** Cutoff to 0%, stop everything.

**Total performance: 2–2.5 minutes.**

---

## Key Reminders

1. **You are the musician.** The synths do not play the song automatically. Every knob turn, every keyboard note, and every timing decision is yours.
2. **Practice the knob movements separately** before the full performance. Get comfortable with the Cutoff sweep and Resonance sweep as isolated actions.
3. **Use a metronome or click track** if available. The TD-3 will sync to the MiniBrute's clock, but you'll need an external click (smartphone app, drum machine, or audio interface) to keep yourself at 124 BPM.
4. **Record your performance.** Once you nail it, capture it on audio. This is a one-time improvisation unless you repeat the exact movements again.
5. **Start at low volumes.** Test each section quietly before taking it to full volume. Feedback can build quickly with high resonance settings.
