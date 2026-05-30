# Felicity Local Testing Fork

This is a personal fork of [Felicity](https://github.com/Hamza417/Felicity), an AGPL-licensed offline music player for Android.

## Disclaimer

This fork is for local testing only. I will not be updating it regularly and highly recommend buying the official license from the original Felicity project:

[https://github.com/Hamza417/Felicity](https://github.com/Hamza417/Felicity)

## Features

### Custom Audio Engine

- **Dual Decoder** utilizing both hardware and software decoding through FFmpeg.
- **Custom DSP:** The entire audio processing chain (EQ, Bass, Reverb) is written in C++ via JNI. It
  utilizes ARM NEON SIMD auto-vectorization to process audio arrays with absolute minimum CPU
  overhead.
  - Supports bass, treble and more.
  - Native downmixing support to pass multichannel audio to stereo output.
- **Advanced Effects:** Integrated spatial effects including stereo widening and tape saturation for
  an analog feel.
- **10-band Equalizer:** A powerful equalizer with 10 adjustable frequency bands up to +/-15 dB with
  dedicated PreAmp support.
- **Gapless Playback:** Seamless transition between tracks without any gaps or interruptions.
- **High-Resolution Audio Support:** Support for high-resolution audio formats such as FLAC, ALAC,
  and DSD for audiophile-grade sound quality.
- **Multi-Channel Audio Support:** Support for multichannel audio formats like 5.1 and 7.1 surround
  sound for an immersive listening experience.
- **Milkdrop Visualizer:** Twin buffer enabled Milkdrop visualizer support powered by a native DSP,
  rendering on GL surface at native fps in real-time.

### User Interface

- **Fully custom-built and highly optimized** interface inspired by Inure App Manager.
- **Dynamic Theming:** The app's theme dynamically adapts to the album art of the currently playing
  track, creating a visually cohesive and immersive experience.
- **Custom Animations:** Smooth and visually appealing animations throughout the app, enhancing the
  user experience and making interactions more engaging.
- **Themes:** Multiple themes including light, dark, AMOLED black, Material You and others.
- **Core:** Predictive back, edge to edge and adapted to all modern Android UI features.
- **Embedded Lyrics:** Reliable, on-the-fly LRC extraction and support for online downloading from
  LrcLib.
- **Dual Fast Scroll:** Simultaneous support for both slide to scroll and jump to letter fast
  scroll.
- **Realtime Audio Visualizer:** A lock-free, zero-allocation visualizer rendering on the Canvas at
  native fps, powered by a native PFFFT implementation.

### Library Management

- **Realtime Library Updates:** The app automatically detects and updates the music library in
  real-time as new tracks are added or removed from the device adapted from Peristyle app.
- **Auto Scanning:** The app automatically scans for new music files and updates the library without
  requiring manual refreshes.
- **Server Mode:** Host Felicity as a local server to create a central music library for all local
  and possibly remote devices through Wi-Fi.

### Smart Core

- **True Randomized Shuffle:** Choose between Miller and Fisher-Yates shuffle algorithms.

This feature list is not exhaustive and only main features are listed.

## License

Felicity Music Player is released as open source software under the
[GNU AGPL v3](https://www.gnu.org/licenses/agpl-3.0.en.html) license. See the
[LICENSE](./LICENSE) file for the full license text.
