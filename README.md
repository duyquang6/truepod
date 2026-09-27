# Truepod

A bit-perfect music player for the **TrimUI Brick Pro**.

*[Tiếng Việt](README.vi.md)*

Every other player on this handheld fixes its output quality at compile time:
44.1 kHz, or 48, or 16-bit. Truepod plays the file at its own rate and bit depth,
and tells you when it could not.

## Download

Pick the build for your firmware from **[the latest release](../../releases/latest)**:

| Firmware | File |
|---|---|
| spruceOS | `Truepod-<version>-spruceOS.zip` |
| stock TrimUI | `Truepod-<version>-stockOS.zip` |

Same player in both. They differ only in which directory the firmware looks in.

## Install

1. Unzip. You get a `Truepod` folder.
2. Copy it onto the SD card. spruceOS: `/mnt/SDCARD/App/`. Stock TrimUI:
   `/mnt/SDCARD/Apps/`. You should end up with `…/Truepod/truepod`.
3. Put music in `/mnt/SDCARD/MEDIA`. Subfolders are how you browse it.
4. Boot the device and open **Truepod**.

## Guide

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

To add music without a card reader, press **Y** in the library and scan the QR
code from a phone on the same network.

## Later

Free keeps the feature set it has now: bug fixes, not new features.

A **Truepod Pro** edition is planned, not released. Sleep timer, favourites,
per-track resume, an editable queue, gapless, a tag index with artist/album
browsing and search, saved playlists, Telegram sync, EQ, hot-switching a USB DAC
on the bottom port, a choice of screen layouts, and more LED modes.

Pro will never gate output quality. There is no quality ceiling in Free and
there will not be one; that is the whole reason this player exists.

## Reporting a problem

Open an issue with your firmware, the version, and `truepod.log` from the app
folder on the card. Its first lines say what your firmware provides, which
usually explains a difference between two devices straight away.


---

Releases and documentation only; the source is not public. Truepod is
proprietary — see [LICENSE](LICENSE).
