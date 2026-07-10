# SG-16 SIGNAL — Complete User Guide

Everything you need to go from a blank machine to a finished, recorded track. Work through it top to bottom the first time; after that, use it as a reference.

---

## 0. Starting Up

1. Open `index.html` (or the live URL) in your browser. **Chrome or Edge are best** — Web Audio and Web MIDI are fully supported there. Safari works for audio but needs a flag for MIDI.
2. You'll see the boot screen. **Click POWER.**
   - Browsers block audio until you click something — POWER is that click. It starts the audio engine.
3. The LCD (the amber screen) lights up. If you've used it before, it says `PROJECT RESTORED FROM AUTOSAVE`. Fresh, it says `NEW PROJECT — DROP SAMPLES ON PADS`.

Everything autosaves to this browser as you go. Close the tab, come back later, your work is still there.

**The five tabs across the top:** GROOVE (main), WAVE (sample editor), MIX (console), SONG (arranger), PERF (master FX). We'll hit all of them.

---

## 1. The Transport & Tempo

The top rail is your control center.

- **PLAY** (or press `SPACE`) — starts/stops the sequencer
- **REC** (or press `R`) — records the master output to a WAV file (Section 8)
- **TEMPO** knob — 50 to 200 BPM. Drag up/down. Hold `Shift` while dragging for fine control
- **SWING** knob — 0 to 60%. Pushes the off-beats late for a shuffled feel
- **MASTER** knob — overall output volume
- **REVERB** knob — the master reverb return level

**Knob tip:** every knob in the machine works the same way — click and drag vertically. Hold `Shift` for fine adjustment. You can also click a knob and use arrow keys.

**Try it now:** Click PLAY. You'll hear nothing yet (no beat programmed), but the STEP LEDs will chase across the top of the sequencer. Set TEMPO to around 90 for hip-hop, ~120 for house. Press SPACE to stop.

---

## 2. The Sampler — Loading & Playing Sounds

The GROOVE page has a 4×4 grid of 16 pads on the left.

### Loading a sample
Two ways:
1. **Drag & drop** an audio file (WAV, MP3, etc.) from your computer directly onto any pad.
2. **Click a pad** to select it, then click **LOAD FILE** and pick a file.

**Example:** Drag a kick drum onto pad 1 (top-left). The pad now shows the filename. Click it — you hear the kick.

### Playing pads
- **Click** a pad to trigger it
- **Keys `1`–`8`** fire pads 1–8
- **`Shift`+`1`–`8`** fire pads 9–16

**Example:** Load a kick on pad 1, a snare on pad 2, a hat on pad 3. Now tap `1`, `2`, `3` on your keyboard — you're finger-drumming.

### Pad controls (the row under the grid)
Select a pad first, then adjust:
- **LOAD FILE / CLEAR** — load or wipe the selected pad
- **MODE** — `ONE-SHOT` (plays the whole sample on tap) or `GATE` (plays only while held)
- **VINTAGE 12-BIT** — engages SP-1200-style 12-bit crunch on that pad. Toggle it on a snare or breakbeat for that gritty, lo-fi character
- **CHOKE GRP** — OFF, 1, 2, 3, or 4. Pads in the same choke group cut each other off

**Choke example (essential for hi-hats):** Put your closed hat on pad 3 and open hat on pad 4. Set **both** to CHOKE GRP 1. Now when the closed hat fires, it silences the open hat — exactly like a real hi-hat pedal. No more overlapping hats ringing over each other.

### The six pad knobs (per pad)
- **GAIN** — volume of this pad
- **PITCH** — transpose ±12 semitones
- **START / END** — trim where the sample starts and stops playing (0–100%)
- **SP CUT / SP RES** — the vintage filter's cutoff and resonance

**Example:** Load a long vocal sample, set START to 20% and END to 35% to isolate just one word.

---

## 3. The WAVE Page — Slicing & Chopping

This is where you turn one sample into many playable hits. Click the **WAVE** tab.

The selected pad's waveform fills the screen. The blue handles are START (left) and END (right).

### Trimming
Drag the blue **START** and **END** handles to top-and-tail the sample — cut silence, isolate a section.

### Chopping into slices
Three ways to place slice markers:
1. **CHOP buttons** (2, 4, 8, 16) — instantly divide the sample into equal slices. `8` gives you eight evenly-spaced chop points
2. **TRANSIENTS** — auto-detects the attacks (drum hits) in the sample and drops markers on them. Perfect for chopping a drum break
3. **Tap the waveform** — manually drop a marker exactly where you click. Tap an existing marker to remove it; drag it to move it

### Turning slices into pads
Once you've got slices, click **SLICES → EMPTY PADS**. Each slice gets mapped to its own empty pad, ready to sequence.

**Full worked example — chopping a drum break:**
1. Drag an 8-bar amen break onto pad 5. Select it.
2. Go to the WAVE tab.
3. Click **TRANSIENTS** — markers appear on every kick and snare hit.
4. Click **SLICES → EMPTY PADS** — each hit is now on pads 6, 7, 8...
5. Go back to GROOVE. Tap those pads with keys — you can now replay the break in any order, or sequence it into a new pattern.

---

## 4. Drum Synthesis & The Step Sequencer

The right side of the GROOVE page is the sequencer — this is where beats are built.

### The drum lanes
There are 8 built-in synthesized drum voices (no samples needed):
- **808 kit:** BD (kick), SD (snare), CH (closed hat), OH (open hat), CB (cowbell)
- **909 kit:** BD, SD, HH

Each lane is a row of 16 step buttons.

### Programming a beat
Click a step to turn it on. **Each click cycles through velocity levels:**
- Off → **HI** (loud) → **MID** → **LO** (soft) → Off

So one click = loud hit, two clicks = medium, three = soft, four = back to off. The color/brightness shows the level.

**Example — a basic house beat:**
1. On the **BD 808** lane, click steps 1, 5, 9, 13 (four-on-the-floor kick)
2. On the **CH 808** lane, click steps 3, 7, 11, 15 (offbeat hats)
3. On the **SD 909** lane, click steps 5 and 13 (backbeat snare)
4. Hit PLAY.

You've got a groove. Click any step a second time to soften it (MID) for dynamics — try making every other hat quieter.

### Pattern length & bars
- **LEN** — 16, 32, 48, or 64 steps. Longer = more room for variation
- **BAR** — when LEN is longer than 16, these buttons page between the 16-step segments

**Example:** Set LEN to 32. Program a basic beat on BAR 1, then click BAR 2 and add a fill (extra snares) so the pattern evolves every two bars.

### The melody lane
The bottom lane (**MEL**) plays melodic notes through a synth.
- **MELODY VOICE** — pick which synth engine plays the melody (P5, JP8, JUNO, etc.)
- **NOTE knob** — sets the pitch for the next note you place
- Click a step to place a note at the current NOTE pitch. Click again to change velocity, same as drums

**Example — a bassline:**
1. Set MELODY VOICE to **JP8** (fat Jupiter bass)
2. Set the NOTE knob to a low note like C2
3. Click steps 1, 4, 7, 11 on the MEL lane
4. To change a note's pitch: set the NOTE knob to a new value, then click that step to retarget it

---

## 5. The Synth Engines

Six polyphonic synths. Whichever you **ARM** (top of GROOVE page, "VOICE ASSIGN") is what your keyboard and MIDI play.

- **P5** — Prophet-class, 5-voice. Warm analog pads and leads
- **JP8** — Jupiter-class, 8-voice. Big, fat, detuned
- **JUNO** — Juno-class with BBD chorus. Lush, classic — toggle CHORUS on for the signature shimmer
- **DX7** — 4-operator FM. Bells, e-pianos, metallic tones. Has ALGORITHM select + E.PIANO/BASS presets
- **OP-FM** — OP-style FM synthesis
- **OP-STR** — OP-style strings

### Playing synths with your keyboard
The computer keyboard becomes a piano:
- **White keys:** `A S D F G H J K L` (and `;`)
- **Black keys:** `W E   T Y U   O P`
- **`Z` / `X`** — shift octave down / up

**Example:** ARM the JUNO. Turn CHORUS on. Play `A S D F G` — you're playing a chord progression on a lush Juno. Hit `X` to jump up an octave.

### Tweaking a synth
Select an armed synth to reveal its knobs — every engine has its own panel plus a shared ADSR envelope (ATTACK, DECAY, SUSTAIN, RELEASE):
- **CUTOFF / RES** — the filter (brightness + resonance)
- **DETUNE / SUB** — thickness and sub-oscillator weight
- **ENV AMT** — how much the envelope opens the filter
- **ATTACK / DECAY / SUSTAIN / RELEASE** — the volume shape over time

**Example — turn a pad into a pluck:** On the JUNO, set ATTACK to minimum and DECAY short with low SUSTAIN. Now it's a short, plucky stab instead of a sustained pad.

---

## 6. The MIX Page — 30-Channel Console

Click the **MIX** tab. Every sound source has its own channel: 16 pads + 8 drums + 6 synths.

Each channel strip has:
- **HI / MID / LO** — 3-band EQ (±12 dB). MID is sweepable (the MID FREQ knob picks which frequencies you're boosting/cutting)
- **PAN** — L/C/R placement in the stereo field
- **SEND** — how much of this channel feeds the master reverb
- **LEVEL** — channel volume (0–125%)
- **M** (mute) / **S** (solo) — SOLO wins over MUTE

**Example — sit the kick in the mix:**
1. Find the **BD 808** channel
2. Boost **LO** for weight, cut a little **MID** so it doesn't clash with the snare
3. Set **PAN** to center (kicks belong in the middle)
4. Nudge **LEVEL** so it sits right under the snare

**Example — widen your hats:** Pan the closed hat slightly left, the open hat slightly right. Add a touch of **SEND** on both for reverb space. Instantly wider, more professional stereo image.

**Solo tip:** Click **S** on any channel to hear it alone — great for dialing in EQ without distraction. Click again to unsolo.

---

## 7. SONG Mode — Building a Full Track

A single 16-step loop is a groove. SONG mode chains grooves into an actual song. Click the **SONG** tab.

### The concept
You save **patterns** (snapshots of your whole grid) into slots **A–H**, then chain them: intro → verse → chorus → drop.

### Saving patterns
1. Build a beat on the GROOVE page (say, a stripped-back intro groove)
2. Go to SONG, set **TAP MODE** to **SAVE**, tap slot **A** → your intro is stored in A
3. Go back to GROOVE, change the beat (add the main drums, a bassline — your fuller "verse")
4. Return to SONG, still in SAVE mode, tap slot **B** → the verse is stored in B
5. Repeat for a chorus in C, a breakdown in D, etc.

**Important:** saving is a snapshot. After you save A, you can freely change the live grid to build B — A is safely frozen and won't change.

### Loading a pattern back
Set **TAP MODE** to **LOAD** and tap a slot to pull it back onto the live grid for editing. (This replaces what's currently on the grid, so save first if needed.)

### Building the chain
1. Set **TAP MODE** to **+ CHAIN**
2. Tap slots in the order you want them to play. Each tap appends to the chain row
3. Tap `A A B B C` → the chain shows `A×1 A×1 B×1 B×1 C×1`

### Adjusting the chain
Each entry in the chain row has controls:
- **− / +** — fewer / more repeats (so `A×4` plays the intro four times before moving on)
- **‹ / ›** — move the entry earlier / later
- **✕** — remove it

**Example chain for a simple track:**
- `A×4` (intro, 4 bars)
- `B×8` (verse, 8 bars)
- `C×8` (chorus, 8 bars)
- `B×4` (back to verse)
- `A×2` (outro)

Set the repeats with the **+** button on each entry.

### Playing the song
1. Set **MODE** to **SONG** (the toggle button — it reads "MODE: SONG" when active)
2. Toggle **LOOP** ON to repeat the whole song, or OFF to stop at the end
3. Hit **PLAY** (or SPACE)

The machine plays through your chain automatically. The LCD shows `SONG A 2/4 [1/5]` — current slot, which repeat you're on, and position in the chain. The playing entry glows red.

**Note:** in SONG mode, playback reads the stored patterns — your live grid stays exactly as you left it, so you can keep tinkering. Switch **MODE** back to **PATTERN** any time to go back to looping the single live grid.

---

## 8. Recording Your Mix to a File

This is how you get audio *out* of the machine. Click nothing special — it works from any page.

### How it works
1. Get your beat or song ready to play
2. Press **REC** (or the `R` key). The REC LED lights red, the LCD starts counting: `REC 00:01`, `REC 00:02`...
3. Everything you do now is captured: hit PLAY to record the sequencer, finger-drum pads live, play synth keys, trigger performance FX — all of it goes into the recording
4. Press **REC** again (or `R`) to stop
5. A **WAV file downloads automatically** — named like `sg16-120bpm-1720200000.wav`

### What gets recorded
The recorder taps the **master output after the limiter** — meaning it captures *exactly what you hear*, including all your mixer settings, reverb, and any performance FX you engage. It's a true bounce of your final sound.

**Example — record an 8-bar loop:**
1. Set your beat playing sounds right in the MIX
2. Stop playback, rewind (STOP resets to the start)
3. Press `R` to arm recording
4. Press SPACE to play — let it run 8 bars
5. Press SPACE to stop the beat, then `R` to stop recording
6. Your WAV is in your Downloads folder, ready to drop into any DAW

**Example — record a full performance:** Start recording, play your whole SONG chain start to finish, and layer in live tape-stops and filter sweeps (Section 9) as it plays. Stop recording — you've captured a complete, performed track in one take.

*Safety note: recording caps at 6 minutes to prevent runaway file sizes.*

---

## 9. PERFORM — Live Master FX

Click the **PERF** tab. These four effects process your entire master output in real time — grab them during playback (and during recording) for movement and drama. They're all **off by default** and completely transparent until engaged.

### FILTER — master lowpass sweep
- Toggle **FILTER ON**
- **CUTOFF** knob sweeps the brightness (120 Hz to 16 kHz)
- **RES** adds resonance/emphasis at the cutoff

**Example — the classic filter-down-then-open:** While a beat plays, engage FILTER and slowly turn CUTOFF down — the track gets muffled, like it's underwater. Then sweep it back up for a satisfying "opening up" build. Bread and butter of electronic music.

### STUTTER — beat repeat (hold to play)
- Choose a rate: **1/4, 1/8, 1/16, 1/32**
- **Hold** the "◉ HOLD TO REPEAT" button — the machine freezes the current slice of audio and loops it as long as you hold
- Release to return to normal

**Example — a snare roll build:** As your beat approaches a drop, set STUTTER to 1/16 and hold the button for two beats. The audio stutters into a tense roll. Set it to 1/32 for the last beat to intensify, then release right on the downbeat. (Do this while recording for an instant pro-sounding transition.)

### TAPE STOP — spin-down
- Set the **TIME** knob (0.25 to 2.0 seconds)
- Click **■ TAPE STOP** — the whole mix pitches and slows down to a dead stop, like yanking the power on a tape deck

**Example — end a section with a slam:** Right at the last beat of your chorus, hit TAPE STOP with TIME around 0.6s. Everything winds down to silence. Perfect dramatic ending or transition into a breakdown.

### GATE — trance chop
- Choose a rate: **1/4, 1/8, 1/16, 1/32**
- Set **DEPTH** (how hard it chops, 0–100%)
- Toggle **GATE ON** — the master volume rhythmically cuts in and out, synced to your tempo

**Example — pump a sustained pad:** Play a long, held synth chord. Engage GATE at 1/16 with DEPTH around 80%. The static chord becomes a rhythmic, pulsing stab pattern — that hypnotic trance-gate effect. When you turn it on during playback, it locks to the next step so it stays in time.

### Stacking FX
You can run several at once — the signal flows FILTER → STUTTER → TAPE → GATE. **Example:** engage GATE for rhythm, then sweep the FILTER down over the top for a filtered, pulsing build. And remember: because they sit on the master, the REC button captures every move.

---

## 10. A Complete Session, Start to Finish

Here's everything tied together — a realistic workflow:

1. **Power on.** Set TEMPO to 92.
2. **Drums.** On GROOVE, program a boom-bap beat: kick on 1 and 11, snare on 5 and 13, hats on the offbeats. Click some hats twice to soften them for a human feel.
3. **Bass.** Set MELODY VOICE to JP8, drop a four-note bassline on the MEL lane down low.
4. **Sample.** Drag a soul vocal onto pad 9. Go to WAVE, trim it to a nice phrase with the blue handles.
5. **Chops.** Hit TRANSIENTS, then SLICES → EMPTY PADS. Now you can replay the vocal rhythmically.
6. **Mix.** On the MIX page: center and boost the kick's LO, pan the hats slightly apart, add SEND reverb to the snare and vocal.
7. **Vintage.** Toggle VINTAGE 12-BIT on the snare pad for grit.
8. **Arrange.** Save this as pattern **A** (SONG tab, SAVE mode). Strip it down (mute the bass, remove some drums), save as intro **B**. Build a chain: `B×4, A×8, B×2`.
9. **Perform & record.** Set MODE to SONG. Press `R` to record, SPACE to play. As it runs, sweep the FILTER during the intro, hold STUTTER before the main section drops, and hit TAPE STOP at the very end.
10. **Done.** Press `R` to stop. Your finished track is a WAV in Downloads — ready to share, or import into a DAW to mix further.

---

## Keyboard Shortcut Reference

| Key | Action |
|-----|--------|
| `SPACE` | Play / Stop |
| `R` | Start / Stop recording |
| `1`–`8` | Trigger pads 1–8 |
| `Shift`+`1`–`8` | Trigger pads 9–16 |
| `A S D F G H J K L ;` | Synth white keys |
| `W E T Y U O P` | Synth black keys |
| `Z` / `X` | Octave down / up |
| `Shift` + drag knob | Fine adjustment |

---

## Quick Troubleshooting

- **No sound?** Make sure you clicked POWER. Check the MASTER knob isn't at zero, and that no channel you need is muted on the MIX page.
- **A sound won't stop / hats ring out?** Set overlapping sounds (like open/closed hats) to the same CHOKE GRP.
- **MIDI keyboard not working?** Use Chrome or Edge. Check the LCD's bottom line — it names your device when connected. See the PERF tab for AUTO/PADS/KEYS routing.
- **Sample too big to save?** Very large samples aren't auto-saved to keep the browser storage healthy — the LCD will tell you. The pattern still works for the session; use smaller/trimmed samples for persistence.
- **Lost your work?** It autosaves to *this browser*. A different browser or a cleared cache starts fresh. For real backups, record your tracks to WAV.

---

*SG-16 SIGNAL — built solo, inspired by classic hardware. Now go make something.*
