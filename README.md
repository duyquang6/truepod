# Truepod

A bit-perfect music player for the **TrimUI Brick Pro**.

*[Tiếng Việt](README.vi.md)*

Every other player on this handheld caps its output at compile time. Truepod
plays the file you actually have — and when the hardware cannot, it says so
instead of pretending.

## Download

Pick the build for your firmware from **[the latest release](../../releases/latest)**:

| Firmware | File |
|---|---|
| spruceOS | `Truepod-<version>-spruceOS.zip` |
| stock TrimUI | `Truepod-<version>-stockOS.zip` |

Same player, packaged for where each firmware looks for apps.

## Install

1. Unzip. You get one folder.
2. Copy that folder into the **`App`** directory at the root of your SD card
   (stock firmware: **`Apps`** — the zip's readme repeats which).
3. Put music in `/mnt/SDCARD/MEDIA`. Subfolders are how you browse.
4. Start the device and open **Truepod**.

## Using it

The buttons on this device are unlabelled, so **SELECT opens the Options
screen, which is the manual** — every binding is listed there.

The ones you need immediately: **A** plays, **B** goes back, **START** is Now
Playing, **L1/R1** change track. Volume is the side buttons.

To get music on without a card reader, open **Wi-Fi upload** in Options and
scan the QR code from a phone on the same network.

## Two things that look like bugs and are not

**"It says CONVERTED."** The built-in speaker runs a fixed 48 kHz clock, so
44.1 kHz music — most music — has to be resampled for it. Truepod reports that
honestly. Plug a USB DAC into the **top** port and the same file plays
BIT-PERFECT. The reading comes from the kernel, not from the player's opinion
of itself.

**"The battery drains while it sits there."** The device will not sleep while
Truepod is open: this firmware's sleep kills playback and never resumed
cleanly, so the player prevents it. Click the **right stick** to blank the
screen with the music still playing, or quit with **MENU** and the device
sleeps normally.

## Diagnostics

The beta sends back **its own log file** after you quit — the `truepod.log` in
the app's folder, which you can read yourself. Never your music, never a
password, and nothing while you are listening. File names in it can be switched
off in Options. The app asks you to agree first; details in
**[Terms](TERMS.md)**.

## Coming later

Free: sleep timer, favourites, per-track resume, an editable queue, gapless.

A **Truepod Pro** edition is planned, not released — a tag index with artist/album
browsing and search, saved playlists, Telegram sync, EQ, and hot-switching a
USB DAC on the bottom port.

Pro will never gate output quality or basic player behaviour. There is no
quality ceiling in Free and there will not be one; that is the whole reason
this player exists.

## Reporting a problem

Open an issue with your firmware, the version, and `truepod.log` from the app's
folder on the card. Its first lines say what your firmware provides, which
usually explains any difference between two devices straight away.


---

Releases and documentation only; the source is not public. Truepod is
proprietary — see [LICENSE](LICENSE).
