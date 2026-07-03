
<img width="839" height="753" alt="image" src="https://github.com/user-attachments/assets/039ddd09-e609-4d73-936b-ee79e6eb59c8" />


@startuml
skinparam componentStyle rectangle
skinparam NoteBackgroundColor #lightyellow
skinparam NoteBorderColor #orange

title Live Studio Rig 2026

package "Master Controller" {
    component [Arturia KeyLab 25] as keylab
}

package "8U Slanted Desktop Rack" {
    component [Korg MS2000BR\n(MIDI Channel 1)] as korg
    component [Behringer K-2\n(MIDI Channel 2)] as k2
}

package "Desktop Module" {
    component [Doepfer Dark Energy II\n(MIDI Channel 3)] as doepfer
}

node "Monitoring" {
    component [Studio Monitors / Interface] as speakers
}

' --- MIDI Connections (Blue) ---
keylab -[#blue,bold]-> korg : "MIDI OUT to MIDI IN\n(5-pin MIDI)"
korg -[#blue,bold]-> k2 : "MIDI THRU to MIDI IN\n(5-pin MIDI)"
k2 -[#blue,bold]-> doepfer : "MIDI THRU to MIDI IN\n(5-pin MIDI)"

' --- Audio Connections (Red/Green) ---
k2 -[#crimson,dashed]-> korg : "Main Out to Audio In 1\n(1/4\" TS Patch)"
doepfer -[#crimson,dashed]-> korg : "Audio Out to Audio In 2\n(1/4\" TS Patch)"
korg -[#forestgreen,bold]-> speakers : "Main L/R Outputs\n(Stereo 1/4\")"

note top of keylab
  **Power Option:**
  Use a 5V USB wall charger
  or a dedicated 5V DC power 
  adapter for standalone use.
end note

note right of korg
  **The Mixer Hub:**
  Korg acts as a digital effects unit 
  for the K-2 and Dark Energy II.
end note

@endum
