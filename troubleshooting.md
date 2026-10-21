---
layout: default
title: Troubleshooting
nav_order: 6
---

# Troubleshooting

## No supported videos found

- Confirm the videos are directly inside the selected folder; BCV does not scan subfolders
- Check that the extension is listed in [Supported Formats](supported-formats)
- Make sure the file is not only a shortcut with a supported-looking name

## A video fails to compress

- Try opening the source video in a media player to confirm it is not corrupt
- Make sure the file is not still being recorded, copied, or used by another application
- Check that the input and output folders are writable
- Try the file on its own in a separate folder to isolate the issue

Some uncommon codecs, damaged files, encrypted media, or streams that FFmpeg cannot decode will not process successfully.

## The output is larger than the original

This can happen when the original already uses an efficient codec or a low bitrate. It can also happen with short videos, high audio settings, or source files that are already heavily compressed.

Try a higher CRF number, such as 25 or 27, or use a slower encoding speed after checking a short test output. Do not assume every source video can be made smaller without a quality trade-off.

## The output quality is not good enough

Use a lower CRF value. Try 21, then 19 if necessary. Lower values preserve more detail but increase file size.

Check action scenes, text overlays, gradients, low-light footage, and important audio, not only a still frame.

## I cannot find the output

The output path is shown in the Output card. By default it is a `compressed` folder inside the input folder, but you can select another destination with **Browse**. After a completed batch, select **Open output folder**.

## The app will not start or FFmpeg cannot be found

Reinstall Batch Compress Video from the [Microsoft Store](https://apps.microsoft.com/detail/9MXZ6FLXKHJF). The app includes its own FFmpeg executable; it does not require a separate system installation.

## Still stuck?

Use **Feedback & support** in the app or email [hello@3thousand30.com](mailto:hello@3thousand30.com?subject=Batch%20Compress%20Video%20support) with the error message, the source file extension, and the settings you selected. Do not send private videos unless you have chosen to share them separately.
