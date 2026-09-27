# Truepod 0.1.0 — first public beta

*Tiếng Việt: [hướng dẫn cài đặt và tính năng](https://github.com/duyquang6/truepod/blob/main/README.vi.md)*

A bit-perfect music player for the TrimUI Brick Pro.

Every other player on this handheld fixes its output quality at compile time:
44.1 kHz, or 48, or 16-bit. Truepod plays the file at its own rate and bit depth,
and tells you when it could not.

Free. The quality is not the paid part, and there is no output ceiling in this
build.

## Download

| Your firmware | File |
|---|---|
| spruceOS | `Truepod-0.1.0-spruceOS.zip` |
| stock TrimUI | `Truepod-0.1.0-stockOS.zip` |

Same player in both. They differ only in which directory the firmware looks in.

## Install

1. Unzip. You get a `Truepod` folder.
2. Copy it onto the SD card. spruceOS: `/mnt/SDCARD/App/`. Stock TrimUI:
   `/mnt/SDCARD/Apps/`. You should end up with `…/Truepod/truepod`.
3. Put music in `/mnt/SDCARD/MEDIA`. Subfolders are how you browse it.
4. Boot the device and open Truepod.

## Features

- Bit-perfect output through a USB DAC on the top port, tested to
  88.2 kHz / 24-bit.
- FLAC, MP3, WAV, OGG, Opus, M4A / AAC / ALAC.
- The browser shows each track's real sample rate and bit depth before you play
  it, with embedded cover art. It remembers the folder you were last in.
- Wi-Fi upload from a QR code, so you can add music without taking the card out.
- A spectrum display on screen, and the RGB LEDs flash to the beat. Both can be
  switched off in Options.
- Screen off with the music still playing.
- Shuffle and repeat all / one / off.
- Delete a track from the browser, with a confirmation.
- Runs on spruceOS and on stock TrimUI firmware.

## Buttons

| Button | Library | Now playing |
|---|---|---|
| D-pad up/down | move the selection | — |
| A | open folder, or play | play / pause |
| B | up one folder | back to the library |
| X | delete the track (asks first) | shuffle on / off |
| Y | Wi-Fi upload | repeat all / one / off |
| L1 / R1 | page up / down | previous / next track |
| L2 / R2 | — | seek 10 seconds |
| START | go to Now Playing | back to the library |

These work on any screen: **SELECT** opens Options, **MENU** quits, the **right
stick click** turns the screen off with the music still playing, and the side
buttons are volume.

## BIT-PERFECT and CONVERTED

The badge says which one you are getting, and it is read from the sound card
rather than from the player.

**BIT-PERFECT** — the samples in the file are what reach the DAC. No software
touched them.

**CONVERTED** — software had to change something on the way, usually the sample
rate. The built-in speaker runs at a fixed 48 kHz, so 44.1 kHz music has to be
resampled for it. A USB DAC on the top port takes the file's own rate, and the
same track plays bit-perfect.

## Known limitations

- The device will not sleep while Truepod is open, so it keeps using battery.
  Quit with MENU and it sleeps normally.
- On stock firmware nothing stops the firmware suspending in the middle of a
  track.
- No gapless playback.
- Tested to 88.2 kHz. Higher rates are untested rather than known bad.

## Free and Pro

Free is frozen at the feature set it has now: bug fixes, not new features.
**Truepod Pro** is planned and not released. It adds a tag index for browsing by
artist and album, search, saved playlists, favourites, an editable queue,
per-track resume, a sleep timer, gapless, EQ, Telegram sync, hot-switching a USB
DAC on the bottom port, a choice of screen layouts, more LED modes, and a
Vietnamese interface.

Feature by feature:
**[Free and Pro](https://github.com/duyquang6/truepod/blob/main/README.md#free-and-pro)**
· **[tiếng Việt](https://github.com/duyquang6/truepod/blob/main/README.vi.md#free-v%C3%A0-pro)**

Pro will never gate output quality. There is no quality ceiling in Free and
there will not be one.

## Something broken?

Open an issue with your firmware, this version, and `truepod.log` from the app
folder. Its first lines say what your firmware provides, which usually explains
a difference between two devices straight away.
