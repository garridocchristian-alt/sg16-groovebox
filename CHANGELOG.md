# SG-16 SIGNAL Changelog

## [v3.0] — July 10, 2026 — "Soft Kits & OP-1 Utilities"

### Added
- **Soft Drum Kit Engine**: The drum voices are now swappable kits selected from a KIT row above the sequencer lanes. Four kits ship:
  - **SP-HYBRID** — the original 808/909 hybrid voices (default; nothing changes for existing patterns)
  - **VELVET** — soft, round, brushed drums in the spirit of Men I Trust "Show Me How": muffled kick, brush snare, airy hats, soft rim, sub-kick, ghost and shaker
  - **DUSK** — dream-pop LinnDrum flavour with a warm tom, soft clap and a shimmer ride
  - **COTTON** — ultra-soft muffled lo-fi kit, everything low-passed and gentle
  Kit choice colours the sound only; lane IDs, mixer channels and saved patterns are untouched, so any kit plays any existing groove. Sequencer lane labels follow the active kit.
- **Tombola (Gravity Sequencer)**: New OP-1-style generative page. Seeds fall under gravity inside a spinning hexagonal drum; every wall strike fires that seed's assigned voice. Choose a target (any drum lane or the armed synth), then ADD SEED or tap inside the drum to drop one where you click. GRAVITY / SPIN / BOUNCE knobs shape the motion; QUANTIZE snaps hits to the 1/16 grid while the transport runs. Up to 24 seeds.
- **Arpeggiator**: Live arp for the armed synth, in the VOICE ASSIGN panel. UP / DOWN / UP-DOWN / RANDOM / ORDER modes, rate from 1/8 down to 1/16T (incl. triplets), ±octave range and a GATE knob. Runs off held keyboard/MIDI notes and follows tempo; fully bypassed when off (held notes sound normally).
- **Tape Warmth**: Always-in-the-path (switchable) master tape colour on the PERFORM page. Continuous wow (0.6 Hz) + flutter (6.4 Hz) pitch drift, tanh saturation drive, a warmth high-shelf and gentle hiss, with a true-bypass dry/wet crossfade. Sits at the end of the master FX chain, just before the limiter.

### Technical
- Master FX chain is now: master → filter → stutter → tape-stop → gate → **tape-warmth** → limiter → out
- Save format bumped v2→v3 (guarded, backward-compatible): stores `kit`, `arp`, `tape` and `tombola` state. Old saves open unchanged; the arp always loads OFF, the tombola transport always loads stopped, and tape-warmth settings persist as a mix choice.
- Tombola physics run only while its page is open (rAF starts on entering, cancels on leaving); triggering is gated by its own transport, so it's silent until you press START.
- Storage key `sg16:project` untouched.

### Known Limitations
- Tombola seed positions are not saved (only each seed's target/note/colour); seeds re-drop from the top on load.
- Arp timing uses a `setTimeout` clock that re-reads BPM each tick — solid for live play, not sample-locked to the main sequencer grid.

---

## [v2.0] — July 5, 2026

### Added
- **Audio Recorder**: REC button captures master output to WAV file (16-bit stereo, post-limiter, includes all FX). Press `R` or click REC. Files auto-named: `sg16-120bpm-<timestamp>.wav`
- **Song Mode**: 8-slot pattern bank (A–H) + chain arranger. SAVE/LOAD/CLEAR pattern snapshots, build chains with repeats, toggle PATTERN/SONG transport mode, loop or stop at chain end
- **Master FX Unit**: Four live performance effects on the master bus (true-bypass design). Filter sweep (LP with resonance), beat-repeat stutter (hold-to-repeat, 1/4–1/32 division), tape-stop emulation (spin-down with pitch fall), tempo-synced gate (trance chop, 1/4–1/32)
- **MIDI Routing Modes**: Three routing behaviors for incoming notes: AUTO (pads when SAMPLER armed, synth otherwise — original behavior), PADS (notes 36–51 always fire pads), KEYS (notes always play armed synth). Multi-device LCD readout shows device name + count

### Technical
- Recorder taps post-limiter, captures performance FX in the mix
- Pattern snapshots are deep-copied; live grid never clobbered during SONG playback
- Pattern advancement at bar boundaries (sample-accurate, sequencer-locked)
- All FX engage/disengage via true-bypass crossfades (off = transparent, zero tone coloration)
- Save format bumped v1→v2 with guarded backward-compatible loads (old saves open unchanged)
- Storage key `sg16:project` untouched

### Known Limitations
- Tape-stop is an emulation (delay-ramp + lowpass + fade), not true varispeed — Web Audio graph doesn't support master playbackRate
- MIDI clock sync intentionally omitted: jitter smoothing fights the lookahead scheduler
- Web MIDI not available in all browsers (notably Safari without a flag); graceful fallback included

---

## [v1.0] — Initial Release

Full-featured browser groovebox:
- 16-pad sampler with waveform editor, transient detection, smart slicing
- Drum synthesis: 808/909 voice library
- Six polyphonic synth engines: Prophet-5, Jupiter-8, Juno w/ chorus, DX7 FM, OP-FM, OP-strings
- 30-channel mixer with 3-band EQ, panning, reverb sends, mute/solo
- Lookahead step sequencer with swing, 16/32/48/64-step lengths
- Hardware-inspired design (SP-1200/TR-808 aesthetic)
- LocalStorage auto-save with full session persistence
- Pure vanilla JS + Web Audio API, no build step, no dependencies
