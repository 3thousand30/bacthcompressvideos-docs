---
layout: default
title: Compression Quality
nav_order: 3
---

# Compression Quality

Batch Compress Video uses a **CRF** quality setting to balance visual quality against file size for either output format.

---

## What CRF means

CRF is a constant-quality control. Lower numbers retain more visual detail and usually create larger files. Higher numbers allow more compression and usually create smaller files.

BCV offers values from **18** to **32** and starts at **23**.

| CRF | Typical result |
|---|---|
| **18–20** | High quality, larger output. A useful choice for material you plan to edit again. |
| **21–24** | Balanced quality and size. Start here for most videos. |
| **25–28** | Stronger size reduction with a higher risk of visible artifacts in fast motion or detailed scenes. |
| **29–32** | Aggressive compression. Use only after checking a representative output. |

Compression results depend on the source codec, resolution, frame rate, motion, grain, and audio. A video that is already efficiently encoded may not become smaller.

---

## Encoding speed

The speed choice controls how much time FFmpeg spends searching for an efficient encode at the selected CRF.

- **Fast** — finishes sooner; useful for quick tests or very large batches
- **Medium** — the default general-purpose balance
- **Slow** — spends longer encoding and may reduce file size at the same CRF

Speed does not change the quality target set by CRF. It changes the time-versus-efficiency trade-off.

---

## Audio bitrate

BCV re-encodes audio as AAC for MP4 or Opus for WebM. Choose:

- **128 kbps** for smaller files where audio quality is less critical
- **192 kbps** as the default for general video
- **256 kbps** when music or detailed audio needs more headroom

---

## A practical testing workflow

1. Copy a representative short video into a test folder
2. Run BCV at CRF 23 and Medium speed
3. Watch the resulting file through to the sections with motion, detail, and important audio
4. Move CRF lower if you see unacceptable artifacts, or higher if the result is still larger than you need
5. Use the selected settings for the full batch

This is more reliable than choosing a CRF by file size alone.
