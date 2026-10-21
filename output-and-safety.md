---
layout: default
title: Output and Safety
nav_order: 5
---

# Output and Safety

Batch Compress Video keeps source files separate from its outputs.

---

## Default output location

BCV starts with a `compressed` folder inside the input folder by default. Select **Browse** in the Output card to choose another destination, or enter an absolute folder path.

The output folder can be anywhere you can write files, but it cannot be the input folder itself. This keeps original videos safe.

---

## Naming output files

Results use the extension for the format selected in the Compression card: `.mp4` for MP4 or `.webm` for WebM.

| Source file | Selected format | Suffix | Output file |
|---|---|---|---|
| `clip.mov` | MP4 | none | `clip.mp4` |
| `clip.mov` | MP4 | `_compressed` | `clip_compressed.mp4` |
| `event.webm` | WebM | `_share` | `event_share.webm` |

---

## Temporary candidates protect originals

For each video, BCV asks FFmpeg to write a temporary candidate in the selected format inside the output folder. It promotes that candidate to the final output name only after FFmpeg completes successfully and the candidate has a non-zero size.

Your input video is never overwritten.

---

## Existing files

With **Skip existing output files** enabled, BCV leaves an existing output file in place and records it as skipped.

With the option disabled, a successfully completed candidate replaces an existing output file with the same name. Use a new suffix or a different output folder if you want to preserve an earlier BCV result.

---

## Cancellation and errors

Selecting **Cancel compression** stops the current FFmpeg process. BCV removes its incomplete temporary candidate and then stops the batch. A failed input is recorded in Activity Logs, and BCV continues with later files unless you cancel the run.
