# Truepod 0.1.1

*Tiếng Việt: [hướng dẫn cài đặt và tính năng](https://github.com/duyquang6/truepod/blob/main/README.vi.md)*

A bit-perfect music player for the TrimUI Brick Pro.

## New in 0.1.1

- **Volume keys work on more USB DACs.** The DAC's volume control is now found
  by what it does rather than by its name, so dongles that call it something
  unusual are no longer skipped. A DAC with no hardware volume says so on the
  Options screen.
- **No more blinking on a track change.** The cover, the tags line and the
  CONVERTED badge stay put until the next track's arrive.
- **SELECT and MENU are shown on Now Playing**, so Options and the way out can
  be found without the manual the device does not have.
- **Installing is unzipping onto the card.** Each zip already carries `App/` or
  `Apps/` for its firmware.
- **The log says what your DAC offers:** its formats, rates and volume control,
  which is what a report about a DAC nobody here owns needs.

<p align="center">
  <img src="https://github.com/duyquang6/truepod/raw/main/media/now-playing.gif" width="300" alt="Now Playing, with the spectrum and the LEDs">
  <img src="https://github.com/duyquang6/truepod/raw/main/media/wifi-sync.jpg" width="300" alt="Wi-Fi upload from a QR code">
</p>

Every other player on this handheld gives something up. Some cap the output at
44.1 kHz or 16-bit, others resample everything to 48 kHz. The side buttons cannot
turn a USB DAC up or down. Playback stutters, skips, or jumps to the next song.
And the screen has to stay on for the music to keep going, which empties the
battery.

Truepod fixes all of that:

- **Full quality.** It plays the file at its own sample rate and bit depth, and
  tells you when it could not.
- **The side buttons control the DAC.** On a USB DAC with a hardware volume,
  the volume keys set it inside the DAC, so the samples themselves are never
  touched. A DAC without one, or that ignores it, keeps its own volume.
- **No stutters, no skipped songs.** The audio gets a CPU core of its own, away
  from the rest of the system. Pausing or replugging the DAC never counts as
  the end of a song.
- **Screen off, music on.** Turn the screen off and the CPU drops to its
  lowest-power setting while the music keeps playing.

Free. The quality is not the paid part, and there is no output ceiling in this
build.

## Download

| Your firmware | File |
|---|---|
| spruceOS | `Truepod-0.1.1-spruceOS.zip` |
| stock TrimUI | `Truepod-0.1.1-stockOS.zip` |

Same player in both. They differ only in which directory the firmware looks in.

## Install

1. Unzip onto the root of the SD card, and merge the folder when asked. The zip
   already carries the right one for your firmware: `App/Truepod` for spruceOS,
   `Apps/Truepod` for stock TrimUI.
2. Put music in `/mnt/SDCARD/MEDIA`. Subfolders are how you browse it.
3. Boot the device and open Truepod.

## Features

✅ in Free, ❌ means it is planned for **Truepod Pro**, which is not released yet.
Free is frozen at what it has now: bug fixes, not new features.

| | Free | Pro |
|---|:---:|:---:|
| Hi-res: 24-bit and high sample rates, tested to 88.2 kHz | ✅ | ✅ |
| Bit-perfect through a USB DAC on the top port | ✅ | ✅ |
| FLAC, MP3, WAV, OGG, Opus, M4A / AAC / ALAC | ✅ | ✅ |
| BIT-PERFECT / CONVERTED read from the sound card | ✅ | ✅ |
| Folder browsing with each track's real rate and bit depth, cover art, delete | ✅ | ✅ |
| Shuffle, repeat all / one / off | ✅ | ✅ |
| Wi-Fi upload from a QR code | ✅ | ✅ |
| Spectrum display, LEDs flashing to the beat | ✅ | ✅ |
| Screen off with the music still playing | ✅ | ✅ |
| spruceOS and stock TrimUI firmware | ✅ | ✅ |
| Browse by artist and album, search, saved `.m3u` playlists | ❌ | ✅ |
| Favourites, an editable queue, per-track resume | ❌ | ✅ |
| Gapless, EQ | ❌ | ✅ |
| Sync and stream music from Telegram, Spotify, SoundCloud and more | ❌ | ✅ |
| Stream from your own music server (Navidrome and other Subsonic servers), bit-perfect | ❌ | ✅ |
| Use the bottom USB port for a DAC | ❌ | ✅ |
| Updates over the air | ❌ | ✅ |
| A choice of screen layouts, more LED modes | ❌ | ✅ |
| Sleep timer | ❌ | ✅ |
| Vietnamese interface | ❌ | ✅ |

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

## Something broken?

[Open an issue on GitHub](https://github.com/duyquang6/truepod/issues/new?template=bug_report.yml) with your firmware, this version, and `truepod.log` from the app
folder. Its first lines say what your firmware provides, which usually explains
a difference between two devices straight away.
