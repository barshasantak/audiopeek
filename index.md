<!-- =========================================================================
     AUDIOPEEK PUBLIC WEBSITE
     Design & Copy by Tara Design Studio
========================================================================= -->

## 📖 The Hero Section
![AudioPeek](https://raw.githubusercontent.com/barshasantak/audiopeek/main/AudioPeek_256.png)
<br>

See Beneath the Waveform.
The native, studio-grade audio specification analyzer and side-by-side A-B diff comparator engineered exclusively for macOS.



    ┌─────────────────────────────────────────────────────────────────────────────────────────────────────┐
    │ 📂 Open File... │ ⚖️ Compare... │ 💾 Export JSON │ 📋 Copy │ Report Font: A- 100% A+ ↺   🔍 Filter  │
    ├─────────────────────────────────────────────────────────────────────────────────────────────────────┤
    │ MASTER_96k24b.wav (File A) │ [ ↔ 2 Mismatches ] │ STREAM_DIST.m4a (File B)                          │
    │ Format: Linear PCM 24-bit 96kHz │ Time Drift: +25.00 ms │ Format: Apple Lossless (ALAC)             │
    ├───────────────────────────────────────┴─────────────────────────┴───────────────────────────────────┤
    │ [AUDIO STREAM DETAILS]                                                                              │
    │ Audio Format Linear PCM (WAV) [DIFF] Apple Lossless (ALAC)                                          │
    │ Sample Rate 96,000 Hz [DIFF] 44,100 Hz                                                              │
    │ Bits Per Sample 24-bit [MATCH] 24-bit                                                               │
    │ Channels 2 (Stereo) [MATCH] 2 (Stereo)                                                              │
    │ Duration 03:45.120 [DIFF] 03:45.145 (Drift: +25.0 ms)                                               │
    └─────────────────────────────────────────────────────────────────────────────────────────────────────┘



## 📖 The Product Story

### *Why we built AudioPeek*

If you work with sound—whether you are a mastering engineer, sound designer, podcaster, or high-resolution audiophile—you encounter a constant frustration: **audio metadata tools are broken**.

* **Command-line utilities like `ffprobe`** are powerful, but memorizing terminal flags and parsing dense text walls halts creative momentum.
* **Legacy tag editors** focus only on artist and album text, completely ignoring the structural reality of the bitstream: *Audio Stream Basic Descriptions (ASBD), true quantization bit depths, pre-skip encoder delays, and uncompressed channel maps.*
* **Cross-platform Electron utilities** lag, consume gigabytes of RAM, and take seconds just to launch.

We asked a simple question: **What if you had a blazing-fast, visually pristine Mac app that reveals the complete DNA of any audio file in under 2 milliseconds?**

AudioPeek was created at **Tara Design Studio** to answer that need. Built from the ground up in 100% native Swift and SwiftUI, AudioPeek taps directly into Apple’s low-level `CoreAudio`, `AudioToolbox`, and `CryptoKit` engines. No web runtimes. No memory bloat. Just pure, instant audio intelligence.



## ⚡ Key Features

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h3>🔍 Deep Bitstream Demuxing</h3>
      <p>Inspect true hardware sample rates, bit depths (16/24/32-bit), channel configurations, MPEG versions, VBR/CBR modes, and container atoms without decoding raw audio into RAM.</p>
    </td>
    <td width="50%" valign="top">
      <h3>⚖️ Side-by-Side A-B Audio Comparator</h3>
      <p>Compare two audio files simultaneously. AudioPeek aligns property keys and instantly highlights format mismatches, sample rate conversions, and missing metadata tags.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>⏱️ Sub-Millisecond Drift Detection</h3>
      <p>Detect encoder latency, leading silence padding, and pre-skip sample offsets (down to 0.1ms) between mastering masters and lossy transcode exports.</p>
    </td>
    <td width="50%" valign="top">
      <h3>🛡️ Hardware-Accelerated SHA-256</h3>
      <p>Stream massive multi-gigabyte DSD or WAV master files in 64 KB binary chunks through Apple Silicon’s hardware cryptographic engine without memory spikes.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🔤 Scoped Report Font Zoom</h3>
      <p>Adjust the reporting table’s typography independently (<code>A-</code> / <code>A+</code> / <code>↺ Reset</code>). Scale the specification tree without breaking your window layout or toolbar chrome.</p>
    </td>
    <td width="50%" valign="top">
      <h3>💾 Sandbox-Safe JSON & Clipboard Export</h3>
      <p>Export single-file or comparative A-B diff reports to formatted JSON with one click using native asynchronous, AppKit-friendly save sheets.</p>
    </td>
  </tr>
</table>



## 🎯 Universal Format Support

AudioPeek parses both uncompressed studio masters and modern web formats:

| Format Category | Supported Codecs & Containers |
| :--- | :--- |
| **Lossless Studio Masters** | **FLAC** (16/24/32-bit), **WAV / Broadcast WAV** (Linear PCM), **AIFF / AIFC** (Apple PCM) |
| **Apple Ecosystem** | **M4A / MP4** (Apple Lossless ALAC, AAC-LC, HE-AAC, Audiobooks) |
| **Modern Streaming & Web** | **Ogg Opus** (48kHz synthesis, pre-skip framing), **Ogg Vorbis** (Nominal/Target Bitrates) |
| **Audiophile & Archival** | **DSD / SACD** (Direct Stream Digital `.dsf`, `.dff` at DSD64 to DSD512), **WavPack** (`.wv`) |
| **Legacy Media** | **MP3** (MPEG-1/2/2.5 Layers I, II, III with CBR/VBR & LAME encoder tags) |



## 🏆 Why AudioPeek is Different

Most diagnostic utilities are bloated ports. AudioPeek is built exclusively for macOS:

    ┌──────────────────────────────────────────────────────────────────────────────────────┐
    │ METRIC                     │ AUDIOPEEK          │ ELECTRON APPS    │ FFPROBE (CLI)   │
    ├────────────────────────────┼────────────────────┼──────────────────┼─────────────────┤
    │ Native macOS Architecture  │ ✅ 100% Swift      │ ❌ Chromium/Node │ ⚠️ C Utility    │
    │ Launch Time                │ ⚡ < 10 ms          │ 🐢 1,500+ ms     │ ⚡ Fast          │
    │ Memory Footprint           │ 🪶 ~ 20 MB         │ 🐘 400 MB - 1 GB │ 🪶 ~ 15 MB      │
    │ Visual A-B Diff Mode       │ ✅ Built-in Split  │ ❌ None          │ ❌ Manual diff  │
    │ Drag & Drop 2 Files        │ ✅ Instant Compare │ ❌ Single file   │ ❌ No GUI       │
    │ ProMotion 120Hz Rendering  │ ✅ Smooth          │ ❌ Frame drops   │ ❌ Terminal     │
    │ Cryptographic Hashing      │ ✅ Hardware NEON   │ ⚠️ Slow JS Pipe  │ ⚠️ Separate md5 │
    └──────────────────────────────────────────────────────────────────────────────────────┘



## ✨ User Experience Highlights

### 1. Dual-Drop Compare Mode
Select two tracks in Finder (like your Master WAV and your Spotify MP3 upload) and drag them together onto AudioPeek. The window instantly transitions into a **two-column comparative diff table**, highlighting mismatches in bold amber and identical parameters in calm green.

### 2. Zero Wait Time on Massive Files
Thanks to non-blocking stream demuxing, dropping a **15 GB DSD256 orchestra master** takes the exact same fraction of a second as opening a **3 MB MP3 voice memo**.

### 3. Native Mac Ergonomics
* Full support for macOS Dark and Light modes.
* Universal keyboard shortcuts (`⌘O` to open, `⌘E` to export, `⌘C` to copy, `⌘+` to scale text, `⇧⌘L` to view logs).
* Multi-column search bar that filters keys and values instantly as you type.



## 🚀 Elevate Your Audio Workflow

Stop guessing what is inside your audio containers. Verify bit depths, confirm sample rate conversions, and validate release metadata with pixel-perfect precision.




## 💬 Help & Support

### Frequently Asked Questions

<details>
<summary><strong>Does AudioPeek alter or modify my audio files?</strong></summary>
<p>No. AudioPeek operates strictly in read-only mode. It inspects container headers and bitstreams without modifying a single byte of your audio data.</p>
</details>

<details>
<summary><strong>Where are diagnostic logs stored?</strong></summary>
<p>AudioPeek maintains rolling daily logs formatted as <code>audiopeek-YYYY-MM-DD.log</code>. You can reveal your log folder directly in Finder anytime by pressing <code>⇧ + ⌘ + L</code> (or via <strong>Help → Show Logs in Finder</strong>).</p>
</details>

<details>
<summary><strong>Is AudioPeek private?</strong></summary>
<p>Yes. AudioPeek is 100% secured. It contains zero analytics, no telemetry, no tracking, and never makes unauthorized network connections.</p>
</details>

<details>
<summary><strong>How do I report a bug or request a new codec?</strong></summary>
<p>You can open an issue or start a discussion on our official <a href="https://github.com/barshasantak/audiopeek/issues">GitHub Issues page</a>.</p>
</details>


### Support

You can report any issues here: [https://github.com/barshasantak/audiopeek/issues](https://github.com/barshasantak/audiopeek/issues){:target="_blank"}

 <br>
 
 <hr>
   <small>© 2026 Santak Das, Tara Design Studio. All rights reserved.</small>
 <br>
