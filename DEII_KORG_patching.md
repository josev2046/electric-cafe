<img width="992" height="1209" alt="image" src="https://github.com/user-attachments/assets/d9bc1a68-3ee0-4fd1-8b21-69a29d2b0195" />

## Hardware Quick-Reference & Cheat Sheet

### Control Voltage (CV) Standards
When patching the Dark Energy II (or connecting it to external gear in the future), keep these electrical standards in mind:
* **Pitch Control:** The Dark Energy II uses the Eurorack standard of 1 Volt per Octave (1V/Oct). Every 1-volt increase from a modulation source raises the pitch by exactly one octave.
* **Gate Signals:** It expects a standard positive Gate signal (usually +5V to +12V) to trigger the ADSR envelope.
* **Modulation CV:** Most modulation inputs (like VCF F or VCO PW) accept signals ranging from -5V to +5V.

### Gain Staging the Hybrid Loop
When routing audio between digital and analogue domains, volume levels drastically change the character of the sound:
* **Korg to Doepfer (Digital to Analogue):** The MS2000BR outputs a hot, line-level signal. When feeding this into the Dark Energy's 'Ext. Audio' input, keep the Korg’s master volume at roughly 50%. Driving it too hard will distort the signal before it even hits the analogue filter.
* **Doepfer to Korg (Analogue to Digital):** Analogue outputs can easily clip digital inputs. If routing the Dark Energy back into the MS2000BR to use its effects, watch the Korg’s input gain stage. If the signal sounds harsh or crackly (and not in a good way), lower the Dark Energy's output volume.

### Essential Troubleshooting Checklist
If you have patched a schematic and cannot hear any sound, run through this diagnostic list before pulling the cables out:

| Component | What to Check | Why it Matters |
| :--- | :--- | :--- |
| **VCA (Amp)** | Is the VCA initial gain turned up, or is it waiting for a Gate signal? | If the amplifier is closed and not receiving an envelope trigger, no sound will pass to the output. |
| **VCF (Filter)** | Is the cutoff frequency turned all the way down to zero? | If the low-pass filter is fully closed, it subtracts all audible frequencies from the oscillator. |
| **Mixer** | Are the VCO and Ext. Audio levels turned up internally? | The Dark Energy requires you to blend the sound sources before they hit the filter. |
| **Modulation** | Is a modulation knob turned up too high? | Extreme LFO or Envelope amounts on pitch (VCO F) can push the audio into subsonic or supersonic ranges, making it seemingly disappear. |

### Default Internal Routings (The 'Normalled' Connections)
Remember that the Dark Energy II is pre-wired internally. You only need patch cables to override or add to these default behaviours:
* **LFO 1** is hardwired to Pitch (VCO F) and Filter Cutoff (VCF F) via the front toggle switches.
* **LFO 2** is hardwired to Pulse Width (VCO PW) via its front toggle switch.
* **The ADSR Envelope** is permanently hardwired to open the Amplifier (VCA), and can be assigned to Pitch, PWM, and Filter Cutoff using the front toggles.
