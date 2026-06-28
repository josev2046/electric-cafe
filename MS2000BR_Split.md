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
