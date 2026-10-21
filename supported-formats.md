---
layout: default
title: Supported Formats
nav_order: 4
---

# Supported Formats

Batch Compress Video accepts common video containers and writes the MP4 or WebM format you select.

---

## Input formats

BCV scans the selected folder for these file extensions:

- MP4 and M4V
- MOV
- AVI
- MKV
- WebM
- WMV
- FLV
- MPEG and MPG
- TS and MTS

The extension identifies files that BCV will offer for processing. A file with a supported extension can still fail if it is corrupted or uses streams that FFmpeg cannot decode.

---

## Output formats

Choose one output format for the whole batch:

| Format | Video | Audio | Best for |
|---|---|---|---|
| **MP4** (default) | H.264, YUV 4:2:0 | AAC | The broadest playback compatibility across devices, apps, and upload services. |
| **WebM** | VP9 | Opus | Web delivery when smaller files are useful and your target supports WebM. |

MP4 is the safer choice when you are unsure. WebM is well-supported by modern browsers, but has less support in older devices and some desktop editing apps.

---

## Why BCV does not preserve the input container

BCV converts all supported inputs to the one output format selected for the batch. This keeps the output folder predictable even if the input folder contains different containers and codecs.

Use the filename suffix option if you want to make converted files easy to distinguish from their originals.
