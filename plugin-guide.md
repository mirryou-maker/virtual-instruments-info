# Imaginary Instruments — user guide

Imaginary Instruments is a free VST3 plugin (Windows/Linux) where every sound is **computed from
physics**, not recorded or sampled. 41 instruments: 12 are shapes with no real-world instrument equivalent at all
(a donut, two overlapping spheres, a 4D/5D hyperball...), and the other 29 are physically-grounded
builds (metal plates, bars, strings, tapped air columns) using the same engine.

## Install

- **Windows**: run the installer (`ImaginaryInstruments-Setup-*.exe`). Installs for the current user,
  no administrator prompt.
- **Linux**: copy `Imaginary Instruments.vst3` to `~/.vst3/` and rescan plugins in your DAW.
- The Windows build isn't code-signed, so Windows SmartScreen may warn on first run — that's expected
  for an unsigned indie release, not a sign anything's wrong.

## The top bar (always visible)

- **Instrument picker** — the dropdown lists all 41 instruments, grouped by family. Entries marked
  **(V)** are the purely imaginary shapes with no real-world equivalent.
- **`<` / `>` buttons** — step to the previous/next instrument in the full list.
- **Help** (top right) — opens this page in your browser.

## The five tabs

### Play
![Play tab, showing the Donut instrument with its shape knob turned and the SFZ/SF2 link](images/guide_play_tab.png)
- **Axis ratio slider** — only does anything for the Oval Drum (1 = round, up to an axis ratio of 2).
- **Shape knob** — morphs the geometry live for the Egg, Donut, Twin Drums, Cone and Two Spheres. Greyed
  out for instruments it doesn't apply to.
- **Mode-ratio chart** — this is the actual overtone spectrum being synthesized right now, not a
  decoration; it updates live as you change instrument/shape/axis ratio and the strike position.
- **SFZ/SF2 link** — under the chart, a link to the sample-pack version of whichever instrument is
  currently selected (see "Sample packs" below).

### Sound (new in 0.9)
![Sound tab, showing Velocity to Brightness, Decay, Material and Strike position on the Piano-like String](images/guide_sound_tab.png)
These shape the sound on top of the computed physics. Each takes effect from the next note you play.
- **Velocity -> Brightness** — how much softer notes lose their upper partials, roughly what happens when
  a soft mallet or finger stays in contact longer. 0 = every velocity has the same spectrum. Loudness
  still follows velocity either way.
- **Decay** — multiplies how long every partial rings (1 = the computed decay times).
- **Material** — makes higher partials die away faster than lower ones. 0 = as computed; around 1
  sounds more like wood.
- **Strike position** — where a string or bar is struck or plucked. A partial whose vibration has a node
  at that point goes quiet: strike a string in the middle and its even harmonics vanish. It works for the
  plucked, piano-like, stiff and bell strings and all six bars (using each bar's computed mode shapes).
  The bowed string has no bow position in its model, and the other instruments keep their computed
  spectrum, so the slider is greyed for them. Turn **Natural** off to move it; with Natural on, each
  instrument uses its own strike point (plucked strings at 1/5 of the length, the piano's hammer rule,
  bars at 0.4 of their length, the kalimba at its tip).

Projects and presets saved with an older version open with these controls at their neutral settings,
so they sound exactly as before.

### Tuning
![Tuning tab, showing the tuning dropdown, Scala .scl/.kbm load buttons and the Reference A4 slider](images/guide_tuning_tab.png)
- Choose equal temperament or one of three experimental scales derived from Bach's Invention No. 2, or
- Load a Scala **`.scl`** scale (and optionally a **`.kbm`** keyboard mapping) to override it with your
  own tuning entirely.
- **Reference A4 (Hz)** — concert pitch, 380 to 480 Hz (440 = standard; double-click to reset, or type
  a value such as 415 or 432). The whole tuning moves with it. It applies to the drop-down tunings and to
  a `.scl` on the default mapping; a loaded `.kbm` and an MTS-ESP master set their own absolute pitch, and
  the tab says so when that is the case.

### Expression
![Expression tab, showing the MPE and MTS-ESP toggles and the retune option](images/guide_expression_tab.png)
- **MPE** — lets a compatible controller bend/pressure each held note independently.
- **MTS-ESP** — follow a tuning broadcast live from an MTS-ESP master plugin elsewhere in your DAW,
  instead of the Tuning tab's own choice.
- **Retune ringing notes when the MTS-ESP tuning changes** — on: notes that are still sounding glide
  to the new pitch when the master changes its tuning. Off: each note keeps the pitch it started with.

### Presets
![Presets tab, showing the preset browser list with a premium entry greyed out](images/guide_presets_tab.png)
- **Save Preset... / Load From File...** — write/read a `.vipreset` file anywhere on disk.
- The list below is a browser: every `.vipreset` found under
  `Documents/Imaginary Instruments/Presets` (searched recursively — a premium pack is just a folder of
  `.vipreset` files dropped in there). Double-click, or select and **Load Selected**.
- Premium presets (marked "(premium)") need an unlock code entered via **Unlock Premium...** before they
  can be loaded.

## The keyboard

Click the on-screen keys, or type on your computer keyboard (A = middle C). Every instrument here is
percussive: notes decay by themselves, and releasing a key does not stop the sound.

## Standalone app: audio output (0.9 and later)

The standalone app (outside a DAW) remembers the audio output you choose in its settings. If that output
disappears for a while, for example a monitor's HDMI audio while the screen sleeps, the app plays through
another device in the meantime and switches back to your chosen output as soon as it returns.

## Sample packs (SFZ/SF2)

Every instrument in the plugin is also available as a royalty-free SFZ/SF2 sample pack, organised by
family — click the link under the mode-ratio chart for whichever instrument you're on, or go straight
to:

- First 10 imaginary instruments: [full set](https://mirryouser.gumroad.com/l/eyojwr) · [free taster (Round Drum)](https://mirryouser.gumroad.com/l/ywlxpw)
- 4 Hyperball instruments: [full set](https://mirryouser.gumroad.com/l/xqkpfk) · [free taster (4D)](https://mirryouser.gumroad.com/l/cshmye)
- 8 metal instruments: [full set](https://mirryouser.gumroad.com/l/hqxlll) · [free taster (Bell)](https://mirryouser.gumroad.com/l/yyjtwt)
- 6 bars: [full set](https://mirryouser.gumroad.com/l/dwjian) · [free taster (Marimba)](https://mirryouser.gumroad.com/l/mnpxtk)
- 5 strings: [full set](https://mirryouser.gumroad.com/l/neyvvzo) · [free taster (Piano-like String)](https://mirryouser.gumroad.com/l/fsnjbf)
- 8 air columns: [full set](https://mirryouser.gumroad.com/l/wvmrdm) · [free taster (Cup-and-Flare Bore)](https://mirryouser.gumroad.com/l/rsvaxh)

## Also available: the free Android app

The same computed-instrument engine (Free Play set) is also available as **Golden Ear: Sound Explorer**
(formerly "Instrument Explorer"), a free Android app with an ear-training quiz mode built around it. See
the [Android app guide](android-guide.html).

## Honest note on realism

The metal, bar, string and tube instruments are computed with solvers checked against exact solutions
or mesh refinement, but none has been compared with a published measurement of a real object. Among the
first 10 (drum-like) instruments, every one is a bounded resonator with a fixed boundary: the Round
Drum reproduces the exact ideal round-membrane solution to five significant figures; the rest are new colours inspired
by a shape, not simulations of real drums or bells.

## Support

Bug reports, questions, anything else: **mirryou@gmail.com**
