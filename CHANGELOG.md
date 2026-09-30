# Changelog

Released builds, newest first. The full announcement for each release is in the
GitHub release itself; this is the short record.

## 0.2.0 — 2026-09-30

Free edition. Full notes: **[RELEASE.md](RELEASE.md)**.

**Fixed**
- Music skipped now and then on the speaker and the jack
- Starting the player turned a USB DAC's volume up to full
- Booting with a DAC plugged in left the buttons unresponsive
- B and START on Options did not return to Now Playing

**Added**
- Rumble on the beat, off by default, with its own Options row

**Changed**
- The built-in output is shown as "Built-in" rather than `audiocodec`

## 0.1.1 — 2026-09-29

Free edition. Full notes: **[RELEASE.md](RELEASE.md)**.

**Fixed**
- Volume keys did nothing on some USB DACs
- Now Playing blinked on every track change: the tags line, the badge and the
  cover each vanished for a moment, and the text beneath jumped up and back
- A long title on a track without cover art printed over the top corner

**Added**
- SELECT (options) and MENU (exit) hints on Now Playing
- The Options screen says when a DAC has no hardware volume
- Each zip carries `App/` or `Apps/`, so installing is unzipping onto the card

**Changed**
- "Beta" is gone from the terms screen

## 0.1.0 — 2026-09-29

First public build. Free edition, for spruceOS and stock TrimUI firmware.
Full notes: **[RELEASE.md](RELEASE.md)**.

**Added**
- Bit-perfect playback through a USB DAC on the top port, at the file's own rate
  and bit depth (verified to 88.2 kHz / 24-bit)
- FLAC, MP3, WAV, OGG, Opus, M4A / AAC / ALAC; shuffle and repeat all / one / off
- Folder browser showing each track's real rate and bit depth before playing,
  with embedded cover art, delete-with-confirmation, and last-folder memory
- Wi-Fi upload from a QR code
- Spectrum visualiser on screen and on the RGB LEDs, with an off switch
- Screen off with the right stick or the power button, music continuing
- Diagnostics: the app's own log uploaded after you quit, consented to on a
  terms screen, with file names switchable off
