# Phatty — Acid · Drums · Poly · FX

**Phatty** is a phat little browser DAW built with the Web Audio API. It combines a classic **TB-303-style acid synth**, a fully-synthesized **808/909-style drum machine**, a fat **subtractive poly synth**, and a rack of **effects** — all on one screen, all synthesized live (no samples). Load a preset, hit play, and twist a knob. The emphasis is squarely on satisfaction and fun, and the 18 presets are affectionate homages to classic tracks.

**[Launch Phatty](https://brendanjameslynskey.github.io/Phatty/)**

---

## Features

- **ACID-303** — monophonic acid voice: switchable saw/square oscillator with a sub octave, a resonant low-pass filter driven by an exponential filter envelope, **accent** (boosts brightness + level + snap) and true legato **slides** (pitch glides between steps), plus a per-voice overdrive for that squelchy growl. Per-step note, accent and slide editing on a 16-step lane.
- **Drum machine** — 8 hand-tuned synthesized voices: kick (pitch-drop + click), snare, 4-burst clap, metallic closed/open hats (with hi-hat choke), two toms and a cowbell. Per-lane **mute/solo** and per-step accent.
- **Poly synth** — 5-voice subtractive synth with dual detuned oscillators, stereo spread, and independent filter + amp ADSR. A 16-step chord sequencer runs chord stabs, basslines and pads.
- **Phat master bus** — warm low shelf → tape-style saturation → glue compressor → brickwall limiter, with a single **PHAT** macro that drives drive, sub weight and squeeze together.
- **Effects** — tempo-synced ping-pong delay send and a decaying-noise convolution reverb send, both fed from every instrument. The sends are **high-passed** so low bass and kick energy never recirculate into the delay feedback or the reverb tail — the repeats stay clean instead of building into a boomy wash.
- **23 presets** — 20 in-the-style-of homages to the best-known electronic records ever made, plus **3 note-accurate reproductions** that transcribe a classic's signature riff step-for-step into the acid lead (see below), plus a **Randomize** button that generates fresh, scale-constrained patterns that always sound musical.
- **Rock-solid transport** — lookahead scheduler (the classic 25 ms / 100 ms "two clocks" pattern) for tight timing, swing, adjustable pattern length (8/12/16), A/B pattern slots with chaining and copy, a glowing playhead synced to the audio, and an analyser-driven VU meter.
- **Custom knobs** — pointer-draggable (mouse and touch), double-tap to reset, mouse-wheel support, with a live value readout.
- **Desktop & mobile** — a responsive layout that auto-detects your device and reflows to a single scrollable column with larger touch targets on phones. Press **Space** to play/stop on desktop.

## Quick start

```bash
python3 -m http.server 8000
# Open http://localhost:8000
```

Or simply open `index.html` in any modern browser — the landing page detects your device and launches the app. On first interaction the app powers on the audio engine (browsers require a user gesture before making sound) and starts jamming.

Best experienced with headphones. 🎧

## Presets — homages to famous tracks

Each of the 20 presets recreates the *feel* of one of the best-known electronic tracks ever made — its signature bassline, drum groove or melodic hook, programmed in Phatty's own voice rather than transcribed. Load one, hit play, and you're in the ballpark of the original in a couple of bars. They span downtempo trip-hop to big beat, trance and filter house (78–138 BPM).

| # | Preset | Genre | Inspired by |
|---|--------|-------|-------------|
| 1 | Globe Trotter | Filter House | Daft Punk — *Around the World* (1997) |
| 2 | Lucky Nights | Disco House | Daft Punk — *Get Lucky* (2013) |
| 3 | Funk Growler | Filter House | Daft Punk — *Da Funk* (1995) |
| 4 | Vienna Smoke | Downtempo | Kruder & Dorfmeister (*K&D Sessions*) |
| 5 | Heartbeat Hymn | Trip-Hop | Massive Attack — *Teardrop* (1998) |
| 6 | Velvet Noir | Trip-Hop | Portishead — *Glory Box* (1994) |
| 7 | Sunshine Bag | Downtempo | Gorillaz — *Clint Eastwood* (2001) |
| 8 | Block Rocker | Big Beat | The Chemical Brothers — *Block Rockin' Beats* (1997) |
| 9 | Spark Punk | Big Beat | The Prodigy — *Firestarter* (1996) |
| 10 | Right About Now | Big Beat | Fatboy Slim — *Right Here, Right Now* (1998) |
| 11 | Slippy Lager | Techno Anthem | Underworld — *Born Slippy .NUXX* (1996) |
| 12 | Sleepless City | Trance | Faithless — *Insomnia* (1995) |
| 13 | Dreamland Keys | Dream Trance | Robert Miles — *Children* (1995) |
| 14 | Dust Devil | Trance | Darude — *Sandstorm* (1999) |
| 15 | Good Feeling | EDM House | Avicii — *Levels* (2011) |
| 16 | Slow Strobe | Progressive House | deadmau5 — *Strobe* (2009) |
| 17 | Cold Monday | Synth / EBM | New Order — *Blue Monday* (1983) |
| 18 | Neon Pulse | Electronic Disco | Giorgio Moroder / Donna Summer — *I Feel Love* (1977) |
| 19 | Automaton | Electro | Kraftwerk — *The Robots* (1978) |
| 20 | Squelch State | Acid Techno | Josh Wink — *Higher State of Consciousness* (1995) |

These are original patterns paying tribute to the tracks that defined each style — no audio or MIDI is copied from the originals.

### Exact-riff reproductions

Three further presets go a step further and transcribe a classic's **signature riff note-for-note** into the mono acid lane (which has per-step pitch), voiced as a bright, low-resonance lead:

| # | Preset | Riff reproduced |
|---|--------|-----------------|
| 21 | Take On Me | a-ha — the Juno intro riff (1985) |
| 22 | Popcorn | Hot Butter / Gershon Kingsley — the Moog melody (1972) |
| 23 | Axel F | Harold Faltermeyer — the *Beverly Hills Cop* theme (1984) |

The synth voice is Phatty's own — only the melody line is reproduced, as a tribute.

## Files

| File | Description |
|------|-------------|
| `index.html` | Landing page with device auto-detection |
| `app.html` | Phatty itself — a single self-contained Web Audio app (responsive; desktop & mobile) |
| `.github/workflows/pages.yml` | GitHub Pages deployment workflow |

## Controls

| Control | Description |
|---------|-------------|
| Power / Play | Powers on the audio engine and starts/stops the transport (or press **Space**) |
| BPM · Swing · Volume | Global tempo, 16th-note swing, and master output level |
| **PHAT** | Macro knob — pushes drive, sub weight and master compression together |
| Preset browser | Prev / Next / dropdown to load a full groove; **Random** generates a new musical pattern |
| A / B · Chain · Copy | Two pattern slots, alternating chain playback, and copy A→B |
| 303 step lane | Click a step to toggle; drag a lit step up/down to change its note; **AC** = accent, **SL** = slide into next note |
| 303 knobs | Cutoff, Reso, Env Mod, Decay, Accent, Tune, Sub, Drive, Level, and Delay/Reverb sends |
| Drum grid | Click steps to program each voice; **M** = mute, **S** = solo; a second click adds accent |
| Poly pads / knobs | Tap a chord pad to cycle chords 1–4; Detune, Cutoff, Env, Attack, Release, Level, and sends |
| FX & Master | Delay time/feedback/tone, reverb size/mix |

## How the phat sound works

"Phat" is not a single control — it is the whole signal chain conspiring to sound big and glued.

**The 303 voice** is a single oscillator through a resonant low-pass filter, but the character lives in the *envelope*: on each note the cutoff jumps up by the Env Mod amount and decays exponentially back down, so every note has a downward "wow." High resonance makes that sweep whistle and squelch. Accented steps push both the envelope depth and the amplitude, and a slide replaces the retrigger with a pitch glide so notes run together the way a real 303's legato does. An overdrive waveshaper after the filter adds the harmonics that turn a clean sweep into acid.

**The drums** are pure synthesis. The kick is a sine whose pitch drops from ~120 Hz to ~45 Hz in a few milliseconds while its amplitude decays, with a short click transient on top for attack — that pitch envelope is what gives an 808 kick its weight. Snares and claps layer filtered noise bursts with tuned tones; hats are clusters of high oscillators through a high-pass, with the closed hat choking the open hat.

**The master bus** is where it all fuses. A gentle low shelf adds warmth, a `tanh` saturation curve rounds off peaks (harmonic thickening rather than harsh clipping), a low-ratio "glue" compressor makes the parts move together, and a fast brickwall limiter keeps the sum loud and controlled. The PHAT macro turns all of these up at once, along with the 303 sub oscillator, so a single knob takes the whole mix from clean to crushed.

Timing is handled by a **lookahead scheduler**: a timer wakes roughly every 25 ms and schedules every note event up to 100 ms into the future against the Web Audio clock, so playback stays sample-accurate even when the main thread is busy — the difference between a groove that pockets and one that stumbles.

---

## A short history of the acid box and the drum machine

### The Roland TB-303 (1981–1984)

Roland released the TB-303 Bass Line in 1981 as a practice tool — a small, cheap box meant to replace a bass guitarist for solo musicians. It paired a single-oscillator synthesizer (sawtooth or square) with a resonant low-pass filter, an envelope with accent and slide, and a famously fiddly step sequencer. As a bass emulator it was unconvincing, and Roland discontinued it in 1984 after selling only around 10,000 units.

Its second life was an accident. The 303's real signature is the interaction of its 18 dB/octave filter, high resonance, and the accent and slide controls: sweep the cutoff with the resonance up while a pattern loops, and the box *squelches*, *whistles* and *growls* in a way no bass guitar ever did. In mid-1980s Chicago, artists began buying the now-cheap, unwanted machines second-hand and misusing them exactly this way.

### The birth of acid house (1986–1988)

The record usually credited with defining the sound is Phuture's *Acid Tracks* (recorded around 1985–86, released 1987) — twelve minutes of a single 303 pattern being tweaked in real time by DJ Pierre. The knob-twisting *is* the composition. The style spread from Chicago house into the UK and Europe, powering the 1988 "Second Summer of Love" and the rave explosion, and "acid" became a genre suffix (acid house, acid techno) denoting that unmistakable 303 timbre.

The lesson the 303 taught electronic music is that an instrument's *misuse* can matter more than its design intent, and that a performance can be the manipulation of a looping machine rather than the playing of notes.

### The drum machines: TR-808 and TR-909 (1980–1984)

Roland's rhythm machines followed a parallel arc. The **TR-808** (1980) synthesized every drum sound with analog circuits rather than samples — its booming, long-decay kick, snappy snare, and metallic cowbell are all pure electronics. Like the 303 it was a commercial disappointment (its drums sounded "unrealistic") and was discontinued by 1983. It then became one of the most sampled and influential instruments in history, foundational to hip-hop, electro and pop.

The **TR-909** (1983) blended analog synthesis (kick, toms, snare) with short digital samples (hi-hats, cymbals) and added MIDI. Its punchier kick and sizzling hats became the backbone of techno and house. Together the 808 and 909 — analog drum synthesis rather than sampling — define the vocabulary that this groovebox recreates: a kick is a pitch-dropping sine, a hat is filtered noise, and character comes from envelopes, not recordings.

### Why it still matters

The 303-plus-drum-machine setup is the archetype of the **groovebox**: a small, immediate, loop-based instrument where you build a pattern and then *play the knobs*. Its enduring appeal is that satisfaction is instant and the feedback loop is tight — exactly the feeling this app is built to deliver in the browser.

---

## License

MIT
