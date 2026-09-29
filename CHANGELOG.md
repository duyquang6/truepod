# Changelog

Released builds, newest first. The full announcement for each release is in the
GitHub release itself; this is the short record.

## 0.1.0 — 2026-09-29

First public build. Free edition, for spruceOS and stock TrimUI firmware.
Full notes: **[RELEASE.md](RELEASE.md)**.

**Added**
- Bit-perfect playback through a USB DAC on the top port, at the file's own rate
  and bit depth (verified to 88.2 kHz / 24-bit)
- Fidelity badge read from the kernel rather than from the player
- FLAC, MP3, WAV, OGG, Opus, M4A / AAC / ALAC; shuffle and repeat all / one / off
- Folder browser showing each track's real rate and bit depth before playing,
  with embedded cover art, delete-with-confirmation, and last-folder memory
- Wi-Fi upload from a QR code
- Spectrum visualiser on screen and on the RGB LEDs, with an off switch
- Screen off with the right stick or the power button, music continuing
- Diagnostics: the app's own log uploaded after you quit, consented to on a
  terms screen, with file names switchable off

**Known limitations**
- The device does not sleep while the app is open
- On stock firmware nothing prevents the firmware suspending mid-track
- No gapless playback
