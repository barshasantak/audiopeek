<!-- =========================================================================
     AUDIOPEEK PUBLIC WEBSITE
     Design by Tara Design Studio
========================================================================= -->

## 🎹 The Hero Section
![AudioPeek](https://raw.githubusercontent.com/barshasantak/audiopeek/main/AudioPeek_256.png)
<br>

### See Beneath the Waveform with AudioPeek.
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

We asked a simple question: **What if you had a blazing-fast, visually pristine Mac app that reveals the complete DNA of any audio file in under 200 milliseconds?**

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

<div style="overflow-x: auto; margin: 24px 0;">
  <table style="width: 100%; border-collapse: collapse; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; font-size: 0.9rem; text-align: left; border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden;">
    <thead>
      <tr style="background: rgba(128,128,128,0.1); border-bottom: 2px solid rgba(128,128,128,0.25);">
        <th style="padding: 12px 16px; width: 30%;">Capability / Metric</th>
        <th style="padding: 12px 16px; width: 25%; background: rgba(0, 113, 227, 0.08); color: #0071e3; font-weight: 700;">AudioPeek</th>
        <th style="padding: 12px 16px; width: 25%;">Electron Tag Editors</th>
        <th style="padding: 12px 16px; width: 20%;">ffprobe (CLI)</th>
      </tr>
    </thead>
    <tbody>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15);">
        <td style="padding: 10px 16px; font-weight: 600;">Native Architecture</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ 100% Swift / CoreAudio</td>
        <td style="padding: 10px 16px;">❌ Chromium / Node.js</td>
        <td style="padding: 10px 16px;">⚠️ C Utility</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15); background: rgba(128,128,128,0.02);">
        <td style="padding: 10px 16px; font-weight: 600;">Launch Time</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">⚡ &lt; 10 ms (Instant)</td>
        <td style="padding: 10px 16px;">🐢 1,500+ ms</td>
        <td style="padding: 10px 16px;">⚡ Fast</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15);">
        <td style="padding: 10px 16px; font-weight: 600;">Memory Footprint</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">🪶 ~ 20 MB</td>
        <td style="padding: 10px 16px;">🐘 400 MB – 1 GB</td>
        <td style="padding: 10px 16px;">🪶 ~ 15 MB</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15); background: rgba(128,128,128,0.02);">
        <td style="padding: 10px 16px; font-weight: 600;">Visual A-B Diff Mode</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ Built-in Split-Table</td>
        <td style="padding: 10px 16px;">❌ None</td>
        <td style="padding: 10px 16px;">❌ Manual diff</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15);">
        <td style="padding: 10px 16px; font-weight: 600;">Time Drift Detection</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ Sub-Millisecond (Δt)</td>
        <td style="padding: 10px 16px;">❌ None</td>
        <td style="padding: 10px 16px;">❌ Manual math</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15); background: rgba(128,128,128,0.02);">
        <td style="padding: 10px 16px; font-weight: 600;">120Hz ProMotion UI</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ Liquid Smooth</td>
        <td style="padding: 10px 16px;">❌ Frame drops</td>
        <td style="padding: 10px 16px;">❌ Terminal only</td>
      </tr>
      <tr>
        <td style="padding: 10px 16px; font-weight: 600;">Hardware SHA-256</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ CryptoKit NEON Engine</td>
        <td style="padding: 10px 16px;">⚠️ Slow JS Pipe</td>
        <td style="padding: 10px 16px;">⚠️ Separate tool</td>
      </tr>
    </tbody>
  </table>
</div>



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

<p style="color: #6e6e73; font-size: 0.9rem; margin-bottom: 20px;">
  💡 <em>Click any question below to expand the answer.</em>
</p>

<div style="max-width: 840px; margin: 0 auto; display: flex; flex-direction: column; gap: 12px;">

  <!-- Question 1 -->
  <details style="border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden; background: rgba(128,128,128,0.02); transition: all 0.2s ease;">
    <summary style="padding: 14px 18px; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; font-size: 1rem;">
      <span>Does AudioPeek alter or modify my audio files?</span>
      <span style="font-size: 0.75rem; color: #0071e3; font-weight: 600; background: rgba(0,113,227,0.1); padding: 4px 10px; border-radius: 999px; white-space: nowrap; margin-left: 12px;">+ View Answer ▾</span>
    </summary>
    <div style="padding: 14px 18px 18px 18px; border-top: 1px solid rgba(128,128,128,0.15); color: #424245; font-size: 0.95rem; line-height: 1.6; background: rgba(128,128,128,0.01);">
      No. AudioPeek operates strictly in <strong>read-only mode</strong>. It inspects container headers and bitstreams without modifying a single byte of your audio data.
    </div>
  </details>

  <!-- Question 2 -->
  <details style="border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden; background: rgba(128,128,128,0.02); transition: all 0.2s ease;">
    <summary style="padding: 14px 18px; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; font-size: 1rem;">
      <span>Where are diagnostic logs stored?</span>
      <span style="font-size: 0.75rem; color: #0071e3; font-weight: 600; background: rgba(0,113,227,0.1); padding: 4px 10px; border-radius: 999px; white-space: nowrap; margin-left: 12px;">+ View Answer ▾</span>
    </summary>
    <div style="padding: 14px 18px 18px 18px; border-top: 1px solid rgba(128,128,128,0.15); color: #424245; font-size: 0.95rem; line-height: 1.6; background: rgba(128,128,128,0.01);">
      AudioPeek maintains rolling daily logs formatted as <code>audiopeek-YYYY-MM-DD.log</code>. You can reveal your log folder directly in Finder anytime by pressing <kbd style="background: rgba(128,128,128,0.15); padding: 2px 6px; border-radius: 4px; font-family: monospace;">⇧ + ⌘ + L</kbd> (or via <strong>Help → Show Logs in Finder</strong>).
    </div>
  </details>

  <!-- Question 3 -->
  <details style="border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden; background: rgba(128,128,128,0.02); transition: all 0.2s ease;">
    <summary style="padding: 14px 18px; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; font-size: 1rem;">
      <span>Is AudioPeek private?</span>
      <span style="font-size: 0.75rem; color: #0071e3; font-weight: 600; background: rgba(0,113,227,0.1); padding: 4px 10px; border-radius: 999px; white-space: nowrap; margin-left: 12px;">+ View Answer ▾</span>
    </summary>
    <div style="padding: 14px 18px 18px 18px; border-top: 1px solid rgba(128,128,128,0.15); color: #424245; font-size: 0.95rem; line-height: 1.6; background: rgba(128,128,128,0.01);">
      Yes. AudioPeek is <strong>100% secure</strong>. It contains zero analytics, no telemetry, no tracking, and never makes unauthorized network connections.
    </div>
  </details>

 <!-- Question 4 -->
  <details style="border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden; background: rgba(128,128,128,0.02); transition: all 0.2s ease;">
    <summary style="padding: 14px 18px; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; font-size: 1rem;">
      <span>Can AudioPeek verify true Hi-Res Lossless formats, bit depths, and multichannel channel layouts?</span>
      <span style="font-size: 0.75rem; color: #0071e3; font-weight: 600; background: rgba(0,113,227,0.1); padding: 4px 10px; border-radius: 999px; white-space: nowrap; margin-left: 12px;">+ View Answer ▾</span>
    </summary>
    <div style="padding: 14px 18px 18px 18px; border-top: 1px solid rgba(128,128,128,0.15); color: #424245; font-size: 0.95rem; line-height: 1.6; background: rgba(128,128,128,0.01);">
      Yes. AudioPeek introspects container headers to verify true quantization bit depth (16-bit, 24-bit, or 32-bit floating point), native sampling rates (44.1 kHz up to 192+ kHz), bitrates (CBR vs. VBR), and channel layouts (Mono, Stereo, 5.1 Surround, 7.1.2/7.1.4 Spatial Audio beds) across FLAC, ALAC, WAV, AIFF, AAC, and MP3 without audio decoding or playback latency.
    </div>
  </details>
  
  <!-- Question 5 -->
  <details style="border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden; background: rgba(128,128,128,0.02); transition: all 0.2s ease;">
    <summary style="padding: 14px 18px; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; font-size: 1rem;">
      <span>How do I report a bug or request a new codec?</span>
      <span style="font-size: 0.75rem; color: #0071e3; font-weight: 600; background: rgba(0,113,227,0.1); padding: 4px 10px; border-radius: 999px; white-space: nowrap; margin-left: 12px;">+ View Answer ▾</span>
    </summary>
    <div style="padding: 14px 18px 18px 18px; border-top: 1px solid rgba(128,128,128,0.15); color: #424245; font-size: 0.95rem; line-height: 1.6; background: rgba(128,128,128,0.01);">
      You can open an issue or start a discussion on our official <a href="https://github.com/barshasantak/audiopeek/issues" style="color: #0071e3; text-decoration: underline; font-weight: 500;">GitHub Issues page</a>.
    </div>
  </details>

</div>


### Support

You can report any issues here: [https://github.com/barshasantak/audiopeek/issues](https://github.com/barshasantak/audiopeek/issues){:target="_blank"}

 <br>
 
 <hr>
   <small>© 2026 Santak Das, Tara Design Studio. All rights reserved.</small>
 <br>
