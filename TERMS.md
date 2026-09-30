# Truepod Beta — Terms

*[Tiếng Việt](TERMS.vi.md)* · Version 1, 2026-09-27

This is a **beta**. It is free, and the thing it asks in return is that it may
send back its own log so bugs can be found and fixed. Using the beta means
agreeing to that.

Plain version of what that means:

## What is sent

After each session, once you have quit the player, it uploads **its own log
file** — the same `truepod.log` sitting in the app's folder on your card. You
can open it and read exactly what is in it at any time.

If there is no network when you quit, the log waits on your card, in
`Saves/truepod/outbox`, and is sent the next time you open or quit Truepod with
Wi-Fi on. It is
deleted from there once it has been received. At most the 20 newest wait.

The log contains:

- Which device and firmware you are on, and which build of Truepod
- What the audio hardware did: sample rates, bit depths, the endpoint opened,
  whether output was bit-perfect or converted
- Errors, timing problems, and recovery attempts
- **The names and paths of files you played.** This is the part you can turn
  off — see below.

A random installation identifier is included so that several logs from one
device can be read together. It is generated on first run and is not derived
from anything about you or your hardware.

## What is never sent

- Your music, or any part of it. Not the audio, not the cover art.
- Any credential, token, pairing code or account detail.
- Your location, contacts, or anything else on the device.

## Turning off the sensitive part

Options has a switch for **file names in logs**. With it off, the player
redacts the names and paths of your music before the log is uploaded. The
technical half — hardware, formats, errors — still goes, because that is what
makes the beta worth running.

The baseline technical log is part of taking part in the beta and is not
switchable. If you would rather send nothing at all, do not install the beta.

## Where it goes and for how long

Reports go to storage controlled by the Truepod authors and are kept for
**60 days**, then deleted automatically. They are used to fix bugs. They are
not sold, not shared with third parties, and not used for advertising.

## No warranty

Beta software, provided as-is, with no warranty of any kind. It plays music on
a handheld; it is not fit for any purpose where failure matters.

## Changes

If these terms change in a way that affects what is collected, the player will
ask again before continuing.

## Contact

Open an issue on this repository.
