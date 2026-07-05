# SG-16 SIGNAL Changelog

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
