---
layout: default
title: Getting Started
nav_order: 2
---

# Getting Started

This guide walks you through compressing your first folder with **Batch Compress Video**.

---

## 1. Install the app

Download **Batch Compress Video** from the [Microsoft Store](https://apps.microsoft.com/detail/9MXZ6FLXKHJF), then launch it from the Start menu.

The first time you open the app, it shows a short Getting Started guide. You can reopen it anytime with the **?** button in the header.

---

## 2. Choose a folder

Select **Browse** in the Input folder card and choose a folder containing videos. BCV scans that folder only; it does not search subfolders.

The Input folder card shows the number of supported videos. If the count is zero, check that the files use one of the [supported formats](supported-formats).

---

## 3. Set quality

Start with the default **CRF 23** setting. It is a sensible balance between size and visual quality for many videos.

- Move toward **18** for higher quality and larger files
- Move toward **32** for stronger compression and smaller files
- Choose **Medium** encoding speed unless you specifically need a quicker run or are comfortable waiting longer for a potentially more efficient encode
- Keep audio at **192 kbps** for a general-purpose default
- Choose **MP4** for the broadest compatibility, or **WebM** when the output is for web delivery

Video compression is lossy. For important footage, test one short video at your intended settings before compressing a large collection.

---

## 4. Choose where files go

By default, results go to a `compressed` folder inside the selected input folder. Select **Browse** to choose any other output folder, or type an absolute folder path. You can also add an optional suffix before the selected extension.

For example, an input file named `holiday.mov` with a suffix of `_small` becomes `holiday_small.mp4` when MP4 is selected, or `holiday_small.webm` when WebM is selected.

Turn on **Skip existing output files** if you want to keep existing output files unchanged when you run the same folder again.

---

## 5. Compress the batch

Select **Compress videos**. The Activity Logs button shows individual successes, skipped files, and errors while the batch runs.

When the batch finishes, BCV displays the number compressed, skipped, and failed, along with the total size change. Select **Open output folder** to inspect the resulting files.

You can select **Cancel compression** during a run. BCV stops the active FFmpeg process and leaves the original video untouched.
