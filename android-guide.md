# Golden Ear: Sound Explorer — user guide

Golden Ear: Sound Explorer is a free Android app that plays **computed instruments**: every sound is generated
on your device from a physics model in real time, not recorded from a real instrument. Nothing is uploaded and
nothing is downloaded; it all happens live as you play.

## Home screen

- **Play today's challenge**: a 10-question listening quiz. Everyone who opens the app on the same calendar
  day gets the same quiz, and it gets harder as you go. If you leave part-way, it picks up where you stopped.
  Once you finish, the button changes to **Review today's result**.
- **Free Play**: pick any of the 41 instruments and play it on the on-screen keyboard. No quiz, no time limit.
- **Skill Check**: the same kind of questions, but you pick the difficulty tier yourself, any time:
  - **Everyday Ears**: comfortable, everyday listening.
  - **Trained Ear**: differences noticeable to a trained musician.
  - **Golden Ear**: the finest differences.
- **What's this?** (next to Skill Check): explains how the quiz works.
- **EAR rating** (top right): a running skill score that starts at 1000. Each answer moves it right away, up for
  correct answers and down for missed ones, and harder questions move it more. It is stored only on your device.
- **Help** (top right): a menu with this guide, the desktop plugin ("Use these sounds in your own music") and the
  privacy policy. The privacy policy is also linked at the bottom right of the Home screen.

## The two kinds of question

- **Shape match**: the same instrument plays the same note in two shapes, A and B. Tap **Play A** and **Play B**
  to listen, then pick the one with the shape the question asks for (for example, the more elongated egg or the
  more tapered cone). Both pictures look the same until you answer; then they show the real shapes.
- **Pitch match**: you hear a reference note (C4), then a mystery note. Tap the mystery note on the keyboard.

After each answer, tap **Next question**. At the end you can **copy your result** and paste it anywhere to
challenge a friend.

## Free Play

Pick an instrument family, then an instrument, and play it on the keyboard (drag or use the arrows to reach
other octaves). Instruments marked **(V)** are purely mathematical shapes with no real-world counterpart (a
donut, two overlapping spheres, a four-dimensional hyperball...); the rest are computed from the same physics a
real instrument of that kind follows (round and oval drums, metal plates, bars, strings, tapped air columns).

- **Shape** slider: changes the shape of the Egg, Donut, Twin Drums, Cone and Two Spheres. The next note you
  play comes from the reshaped instrument; a note that is already ringing keeps its shape.
- **Axis ratio a/b** slider: changes the Oval Drum, from round to twice as long as it is wide.
- **Ring length (Decay)** slider: how long notes ring, for every instrument (0.25 to 4 times; 1 = as computed,
  the default). Strings and some drums ring for many seconds; turn it down for shorter notes. Double-tap to reset.
- Sliders that don't apply to the selected instrument are dimmed.
- **Help** (top right): the same menu as on the Home screen, plus the sample pack for the instrument you have selected.

## Language

The app follows your phone's language. On Android 13 or newer you can also pick a language for this app only:
**Settings > Apps > Golden Ear: Sound Explorer > Language**. Currently available: English and Korean.

## Using these sounds on a computer

The same instruments are available as **Imaginary Instruments**, a free plugin (VST3 and CLAP for Windows and
Linux, LV2 on Linux, plus a standalone Windows app) that works inside a DAW (REAPER, Cubase, Ableton Live, FL Studio,
Bitwig Studio and others). The plugin adds sound-shaping controls, Scala (`.scl`/`.kbm`) and `.tun` microtonal
tuning, MPE and MTS-ESP support, and each instrument family is also available as an SFZ/SF2 sample pack.

**Get it here: <https://mirryouser.gumroad.com/l/dfgpat>**

Inside the app, open **Help** and choose **Use these sounds in your own music**. In Free Play the same menu also
opens the sample pack for the instrument you have selected.

## Privacy

Golden Ear: Sound Explorer collects no personal data at all. See the [Privacy Policy](privacy-policy.md) for
details.

Questions or bug reports: mirryou@gmail.com
