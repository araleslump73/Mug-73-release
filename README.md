**English** · [Italiano](README.it.md)

# Mug-73

A 1970s-style monophonic synthesizer (with an optional polyphonic mode): three oscillators, a 24 dB/oct ladder filter, two envelopes, LFO, arpeggiator, step sequencer, a full effects chain and an external audio input. It runs as a **CLAP plugin** in your DAW and as a **standalone app** on Windows, macOS and Linux.

**[Download the latest release](../../releases/latest)**

[☕ Support Mug-73 on Ko-fi](https://ko-fi.com/mat73)

> The source code is not published. This repository holds the downloads, the documentation and the issue tracker.

## What's inside

- **Voice**: 3 oscillators (6 waveforms, 6 ranges), noise (white/pink), mixer with overload, 4-pole ladder filter with emphasis and contour, two ADSR envelopes, LFO (free or tempo-synced) with five destinations. Mono or poly (2–8 voices).
- **EXT channel**: voice, guitar or any track enters the mixer like an oscillator and goes through the filter and the envelope (gated or drone). In a DAW it uses a sidechain input; in the standalone app you pick an audio input in Settings.
- **Arpeggiator and 16-step sequencer** that follow the DAW tempo and transport.
- **Effects**: drive, compressor, 3-band EQ, phaser/flanger, chorus, rotary speaker, delay (mono/ping-pong), reverb.
- **170 factory presets** in 12 groups; save your own, edit the preset file by hand, export and import.
- **MIDI**: pitch bend, mod wheel, program change, MIDI Learn on every control.
- Very light on the CPU (about 2–3% of one core with all effects on), so small buffers are fine.

## Install

1. Download the zip for your system from **Releases** and unzip it.
2. Copy `Mug-73.clap`:
   - **Windows**: `C:\Program Files\Common Files\CLAP\`
   - **macOS**: `~/Library/Audio/Plug-Ins/CLAP/`, then run `xattr -dr com.apple.quarantine ~/Library/Audio/Plug-Ins/CLAP/Mug-73.clap` (the files are not signed)
   - **Linux**: `~/.clap/`
3. Rescan plugins in your DAW: **Mug-73** appears among the instruments.

The files are not digitally signed, so Windows SmartScreen may warn you the first time.

For the lowest latency on Windows use the ASIO driver of your audio interface in the DAW with a 64–256 sample buffer.

> **VST3** is not offered: the VST3 bindings available for this plugin framework are GPLv3, which is not compatible with closed-source distribution. Use the CLAP version (supported by Bitwig, REAPER, FL Studio, Studio One, MultitrackStudio and others) or the standalone app.

## Standalone app

Run `Mug-73` (`Mug-73.exe` on Windows). It plays through the system audio output and connects the first MIDI keyboard it finds. You can also play the on-screen keyboard or the PC keyboard (A W S E D F T G Y H U J K O L P; Z/X change octave; Space starts the sequencer).

```
Mug-73 --midi-input ""         list MIDI inputs
Mug-73 --midi-input "name"     use that input
Mug-73 --output-device ""      list audio outputs
Mug-73 --period-size 128       buffer in samples
Mug-73 --help                  all options
```

Settings (output level, audio output, **audio input for EXT**, buffer, MIDI input, interface size) are saved and applied by restarting the app. The audio input is off at first so that an open microphone cannot feed back: use headphones.

## Feedback

Bugs and requests: open an [issue](../../issues). Please include your system, DAW and plugin version.

## Support

Mug-73 is free. If it is useful to you, you can support its development with a tip on [Ko-fi](https://ko-fi.com/mat73). Thank you!

## Licence

Free to use, including for music you release or sell; not for redistribution. See [LICENSE.txt](LICENSE.txt). Third-party components: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
