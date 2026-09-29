# Truepod 0.1.0

*Tiếng Việt: [hướng dẫn cài đặt và tính năng](https://github.com/duyquang6/truepod/blob/main/README.vi.md)*

A bit-perfect music player for the TrimUI Brick Pro.

Every other player on this handheld gives something up. Some cap the output at
44.1 kHz or 16-bit, others resample everything to 48 kHz. The side buttons cannot
turn a USB DAC up or down. Playback stutters, skips, or jumps to the next song.
And the screen has to stay on for the music to keep going, which empties the
battery.

Truepod fixes all of that:

- **Full quality.** It plays the file at its own sample rate and bit depth, and
  tells you when it could not.
- **The side buttons control the DAC.** With a USB DAC, the volume keys set the
  DAC's own hardware volume, so the samples themselves are never touched.
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

## Known limitations

- The device will not sleep while Truepod is open, so it keeps using battery.
  Quit with MENU and it sleeps normally.
- On stock firmware nothing stops the firmware suspending in the middle of a
  track.
- No gapless playback.
- Tested to 88.2 kHz. Higher rates are untested rather than known bad.

## Something broken?

Open an issue with your firmware, this version, and `truepod.log` from the app
folder. Its first lines say what your firmware provides, which usually explains
a difference between two devices straight away.
