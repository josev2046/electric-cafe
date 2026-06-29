# Split Patch (Drum Machine & Acid Synth)

## Global Setup
* **Mode:** Split.
* **Timbre Voice:** 1+3 or 2+2 (As the drum track is a monophonic rhythm, 1 voice is sufficient, leaving the remainder for the synth).
* **Split Point:** Set this to a comfortable key to trigger the drums with the left hand and the synth with the right.
* **Tempo:** 120 BPM.

---

## Left Split (Timbre 1): The Drum Machine
Synthesise a kick drum from an oscillator and use the noise generator for the hats/snare. Use the Mod Sequencer to create the rhythm.

* **Voice Assign:** Mono.
* **Oscillator 1 (Kick):** Sin. Tune it low.
* **Oscillator 2 (Hats/Snare):** Noise.

### Mod Sequencer Routing & Values
* **SEQ COMMON:** Set Seq Type to Forward and Key Sync to Timbre or OFF to ensure the drum loop runs consistently.
* **SEQ 1 DEST:** NoiseLvl (Noise Level).
* **SEQ 1 Values (Steps 1–16):** `0, 60, 40, 60, 100, 60, 40, 60, 0, 60, 40, 60, 100, 60, 40, 60`
  * *Note: The values of `100` on steps 5 and 13 mimic a snare accent on beats 2 and 4. The alternating `60` and `40` values create a dynamic, 16th-note closed/open hi-hat feel.*
 
### ALternative Left Split (Timbre 1): Robotnik #1
Ensure the **TIMBRE SELECT [SELECT]** key has the **1** LED lit so you are editing the left side of the split. We need the synth to stay "open" so the sequencer can do the rhythmic work, and we need the filter wide open so the noise sounds like crisp hi-hats.

**The Sound:**
* **Voice Assign:** Press **SELECT [2]** to go to Page 03A: VOICE. Use the **[-/NO]** key to set `Assign:` to **Mono**.
* **Amp Envelope:** Press the **AMP [EG 2 / GATE]** key until the LED is **LIT**. This puts it in `GATE` mode, meaning the sound stays at full volume as long as you hold a key down, allowing the sequencer to carve out the rhythm.
* **Filter:** Turn the **FILTER [CUTOFF]** knob all the way up to **127 (Max)**. This ensures your hats are bright and fizzy. (It will not affect the kick, as sine waves have no overtones to filter).

**The Oscillators (Zeroing the Mix):**
Because the Mod Sequencer adds *offsets* to the current knob positions, we must start with a silent mix.
* **Kick Drum (OSC 1):** Press the **OSCILLATOR 1 [WAVE]** key until the `CROSS` (Sine) LED lights up. Turn the **[CONTROL 1]** knob all the way down to **0**. Use the **[TUNE]** knob to pitch it down low.
* **Hats/Snare (Noise):** You are using the Noise generator for this.
* **The Crucial Step:** Turn the **MIXER [OSC 1]**, **[OSC 2]**, and **[NOISE]** knobs all the way down to **0**. The synth should currently make no sound if you press a key.

**The Sequence:**
* **Routing Setup:** Press **SELECT [11]** to jump to the Sequencer menu. Press **CURSOR [>]** to Page 18B and ensure `Seq Type:` is **Forward**. Press **CURSOR [>]** twice to Page 18D and set `Key Sync:` to **Timbre**.
* **SEQ 1 (The Kick Drum):** Press the **SEQ EDIT [SELECT]** key on the far left until the **SEQ 1** LED is lit. Give the **MIXER [OSC 1]** knob a quick wiggle. The screen will automatically assign SEQ 1 to `OSC 1 Level`.
  * *Entering Steps:* Using the 16 knobs along the bottom, dial in a 4-to-the-floor kick pattern by turning steps 1, 5, 9, and 13 up to maximum (+63), and leaving everything else at 0.
  * *Values:* `63, 0, 0, 0, 63, 0, 0, 0, 63, 0, 0, 0, 63, 0, 0, 0`
* **SEQ 2 (The Hats and Snare):** Press the **SEQ EDIT [SELECT]** key until the **SEQ 2** LED is lit. Give the **MIXER [NOISE]** knob a quick wiggle. The screen will automatically assign SEQ 2 to `NoiseLvl`.
  * *Entering Steps:* Using the 16 knobs, dial in your alternating hi-hat and snare accent pattern.
  * *Values:* `0, 63, 40, 63, 63, 63, 40, 63, 0, 63, 40, 63, 63, 63, 40, 63`
* Turn on the **MOD SEQUENCE [ON/OFF]** button to hear it run.


### ALternative Left Split (Timbre 1): Robotnik #2

#### 1. Voice & Amp Settings (Bypassing the Standard Envelope)
* **Press [EDIT]** to enter LCD Edit Mode.
* **Press SELECT [2]** -> Go to Page `03A: VOICE Assign` -> Use [+/YES] to set to **Mono**.
* **Press AMP [EG 2 / GATE]** on the front panel until the LED is **LIT** (Gate Mode).

#### 2. LFO 1 Setup (Creating the Custom Drum Envelope)
* **Press SELECT [8]** -> Go to Page `12A: LFO1 Wave` -> Set to **Saw**.
* **Press CURSOR [>]** -> Go to Page `12B: LFO1 KeySync` -> Set to **Timbre**.
* **Press CURSOR [>]** -> Go to Page `12C: LFO1 TempoSync` -> Set to **ON**.
* **Press CURSOR [>]** -> Go to Page `12D: LFO1 Sync Note` -> Set to **1/16**.

#### 3. Virtual Patch Routing (Mapping the Punch)
* **Press VIRTUAL PATCH 1 [SELECT]** -> Go to Page `14A: PATCH1`.
  * Move cursor to `Source` -> Set to **LFO 1**.
  * Move cursor to `Dest` -> Set to **Amp**.
  * Move cursor to `Intensity` -> Set to **+63**.
* **Press VIRTUAL PATCH 2 [SELECT]** -> Go to Page `15A: PATCH2`.
  * Move cursor to `Source` -> Set to **LFO 1**.
  * Move cursor to `Dest` -> Set to **Pitch**.
  * Move cursor to `Intensity` -> Set to **+24** (Adjust this later to tune the kick's "zap").

#### 4. Oscillator, Filter & Mixer (Zeroing the Base Sound)
* **OSC 1 (Kick):** Press front panel **OSCILLATOR 1 [WAVE]** to **CROSS**. Turn **[CONTROL 1]** knob to **0**.
* **Filter:** Turn front panel **FILTER [CUTOFF]** knob up to **127**.
* **Mixer Setup:** * **Press SELECT [7]** -> Go to Page `07A: MIXER OSC 1 Level` -> Set to **0**.
  * **Press CURSOR [>]** -> Go to Page `07B: MIXER OSC 2 Level` -> Set to **0**.
  * **Press CURSOR [>]** -> Go to Page `07C: MIXER Noise Level` -> Set to **0**.

#### 5. Mod Sequencer Routing (The Engine)
* **Press SELECT [11]** -> Go to Page `18A: SEQ COMMON`.
* **Press CURSOR [>]** -> Go to Page `18B: Seq Type` -> Set to **Forward**.
* **Press CURSOR [>]** twice -> Go to Page `18D: Key Sync` -> Set to **Timbre**.

#### 6. Programming the Steps (The Groove)
* **SEQ 1 (Kick Drum):** * Press **SEQ EDIT [SELECT]** until **SEQ 1** is lit -> Page `19A: SEQ1 Knob`.
  * Set to **OSC 1 Level**.
  * Twist the 16 bottom knobs to enter values: `63, 0, 0, 0, 63, 0, 0, 0, 63, 0, 0, 0, 63, 0, 0, 0`.
* **SEQ 2 (Hi-Hats):**
  * Press **SEQ EDIT [SELECT]** until **SEQ 2** is lit -> Page `20A: SEQ2 Knob`.
  * Set to **NoiseLvl**.
  * Twist the 16 bottom knobs to enter values: `0, 63, 40, 63, 0, 63, 40, 63, 0, 63, 40, 63, 0, 63, 40, 63`.
* **SEQ 3 (Snare Accent):**
  * First, turn the front panel **FILTER [CUTOFF]** knob down to **40**.
  * Press **SEQ EDIT [SELECT]** until **SEQ 3** is lit -> Page `21A: SEQ3 Knob`.
  * Set to **Cutoff**.
  * Twist the 16 bottom knobs to enter values: `0, 0, 0, 0, 63, 0, 0, 0, 0, 0, 0, 0, 63, 0, 0, 0`.

Turn on the **MOD SEQUENCE [ON/OFF]** button, press a key, and let it run!
---

## Right Split (Timbre 2): The Acid Synth
This configuration dedicates the entire right Timbre to the synth, providing all three Mod Sequence lanes. This allows for a generative arpeggiator setup alongside independent filter and decay sequencing.

* **Voice Assign:** Mono (or Unison for a thicker, slightly detuned sound).
* **Oscillator 1:** Saw or Squ (Classic 303 waveforms).
* **Filter:** 24LPF for a steeper, squelchier cutoff. Turn up the Resonance.

### Arpeggiator Setup (For generative pitch chaos)
* **Target:** Timbre 2 (Ensures it only scrambles the synth, not the drums).
* **Type:** Random.

### Mod Sequencer Routing & Values
* **SEQ COMMON:** Seq Type set to Forward. Key Sync MUST be OFF so the Arpeggiator does not constantly reset the sequence steps.
* **SEQ 1 DEST:** Pitch. 
  * *Note: If you are using the random Arpeggiator trick above, you can turn this off or map it elsewhere (e.g., Pan or LFO Speed). If you turn the Arpeggiator OFF and want the exact melodic sequence from the original groove, use the semitone offsets below.*
  * **SEQ 1 Values (Steps 1–16):** `+12, 0, +12, 0, +15, 0, +12, 0, +19, 0, +15, 0, +12, 0, +15, 0`
* **SEQ 2 DEST:** Cutoff. 
  * **SEQ 2 Values (Steps 1–16):** `+40, 0, +20, 0, +40, 0, +20, 0, +50, 0, +40, 0, +20, 0, +40, 0`
  * *Note: These are positive relative offsets. They rhythmically open the filter to recreate the stepping acid modulation.*
* **SEQ 3 DEST:** Amp (Volume).
  * **SEQ 3 Values (Steps 1–16):** `+63, 0, 0, 0, +63, 0, 0, 0, +63, 0, 0, 0, +63, 0, 0, 0`
  * *Note: This maps maximum relative volume accents to the downbeats (steps 1, 5, 9, 13), creating rhythmic gating and a heavy 4-to-the-floor pulse beneath the chaos.*
 
---

## Programming

Before beginning, note a hardware reality of the MS2000 series: Noise is not Oscillator 2. It is a completely independent sound source with its own dedicated volume knob in the `MIXER` section. This means you do not have to sacrifice an oscillator to generate hi-hats.

Here is the step-by-step guide to programming this patch from a blank slate.

### 1. Initialise the Programme
Wipe the slate clean to ensure no lingering settings interfere with your new patch.
* Press the **[EDIT]** key to enter LCD Edit mode.
* Press the **SELECT [16]** key (the 16th step key along the bottom). The screen will show Page 26A: UTILITY `InitProgram`.
* Press the **[+/YES]** key twice to confirm the initialisation.

### 2. Global Setup (The Split)
* Press **SELECT [1]** to go to Page 01A: COMMON. 
* Use the **[+/YES]** key to change `Mode:` from Single to **Split**.
* Press the **CURSOR [>]** key to move to Page 01B. Change `Timbre Voice:` to **1+3** or **2+2**.
* Press the **CURSOR [>]** key again to move to Page 01C. Change `Split Point:` to your preferred key by using the **[+/YES]** and **[-/NO]** keys.
* Turn the **ARPEGGIATOR [TEMPO]** knob until the screen reads `120`.

### 3. Left Split (Timbre 1): The Drum Machine
Ensure the **TIMBRE SELECT [SELECT]** key has the **1** LED lit so you are editing the left side of the split.

**The Sound:**
* **Voice Assign:** Press **SELECT [2]** to go to Page 03A: VOICE. Use the **[-/NO]** key to set `Assign:` to **Mono**.
* **Kick Drum (OSC 1):** Press the **OSCILLATOR 1 [WAVE]** key until the `CROSS` (Sine) LED lights up. To make it a pure Sine wave, turn the **[CONTROL 1]** knob all the way down to **0**. Use the **[TUNE]** knob to pitch it down low for a deep kick.
* **Hats/Snare (Noise):** Turn the **MIXER [NOISE]** knob up. Turn the `OSC 1` and `OSC 2` mixer knobs down so you only hear noise while you sculpt it.

**The Sequence:**
* **Routing:** Press **SELECT [11]** to jump to the Sequencer menu. 
* Press **CURSOR [>]** to Page 18B and ensure `Seq Type:` is **Forward**. 
* Press **CURSOR [>]** twice to reach Page 18D and set `Key Sync:` to **OFF**.
* **Assigning SEQ 1:** Press the **SEQ EDIT [SELECT]** key on the far left until the **SEQ 1** LED is lit. The screen will show Page 19A. Use the **[+/YES]** key to change `Knob:` to **NoiseLvl**.
* **Entering Steps:** Using the 16 knobs along the bottom, dial in the values: `0, 63, 40, 63, 63 (Max), 63, 40, 63, 0, 63, 40, 63, 63 (Max), 63, 40, 63`. Turn on the **MOD SEQUENCE [ON/OFF]** button to hear it run.

### 4. Right Split (Timbre 2): The Acid Synth
Press the **TIMBRE SELECT [SELECT]** key so the **2** LED is lit. You are now editing the synth side.

**The Sound:**
* **Voice Assign:** Press **SELECT [2]**. Change `Assign:` to **Mono** or **Unison**.
* **Oscillator:** Press the **OSCILLATOR 1 [WAVE]** key to select the **Saw** or **Squ** LED.
* **Filter:** Press the **FILTER [FILTER TYPE]** key to select **24LPF**. Turn up the **[RESONANCE]** knob.

**The Arpeggiator:**
* Press **SELECT [15]**. The screen will show Page 25A. Set `Type:` to **Random**.
* Press **CURSOR [>]** until you reach Page 25E `Target:`. Set this to **Timbre 2**.
* Press the **ARPEGGIATOR [ON/OFF]** button so the LED is lit.

**The Sequence:**
* **Routing:** Press **SELECT [11]**. Press **CURSOR [>]** to Page 18B and ensure `Seq Type:` is **Forward**. 
* Press **CURSOR [>]** to Page 18D and set `Key Sync:` to **OFF** (this is vital to stop the Arpeggiator from resetting the sequence).
* **SEQ 1 (Pitch):** Press **SEQ EDIT [SELECT]** until **SEQ 1** is lit. Change `Knob:` to **Pitch**. Input your melody offsets using the 16 knobs. *(Skip step entry if relying purely on the Arpeggiator).*
* **SEQ 2 (Cutoff):** Press **SEQ EDIT [SELECT]** until **SEQ 2** is lit. Change `Knob:` to **Cutoff**. Input your positive filter offsets using the 16 knobs.
* **SEQ 3 (Amp):** Press **SEQ EDIT [SELECT]** until **SEQ 3** is lit. Change `Knob:` to **Amp**. Dial steps 1, 5, 9, and 13 to maximum, and the rest to 0. Turn on the **MOD SEQUENCE [ON/OFF]** button for Timbre 2.

### 5. Save Your Patch (The Write Operation)
If you turn off the synth now, you will lose everything.
* **Turn off Memory Protect:** Press the **[GLOBAL]** key. Press **SELECT [4]** to reach Page 2A: MEMORY `Protect:`. Press the **[-/NO]** key to turn it **OFF**.
* **Write the Patch:** Press the **[WRITE]** key. 
* The screen will say `WR Prog: A01 OK?`. Use the **[+/YES]** and **[-/NO]** keys to choose the bank and slot where you want to save it. 
* Press **[WRITE]** one final time. The screen will display `Completed`.

