# Wanwan OKI ADPCM ROM editor

This folder contains a dependency-free browser editor for generating a replacement OKI MSM6653A-457 phrase ROM binary for Wanwan Aijou Monogatari.

Open `index.html` in a modern browser. Users can upload WAV, MP3, OGG, FLAC, M4A, or other audio formats supported by the browser's `decodeAudioData()` implementation. The editor mixes to mono, trims optional silence, applies a DC blocker, resamples to the selected OKI rate, encodes to the same 4-bit OKI ADPCM model used by CLoopy, and exports a 128-entry phrase-table ROM binary.

Only command slots 0x13 and 0x16 are named in the UI because they are grounded by save-state traces. Other command slots are shown as guesses, using assumptions from the earlier original-sample categories rather than the free replacement pack.
