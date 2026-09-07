# NDial Recorder

Call recording companion for [NDial](https://play.google.com/store/apps/details?id=com.hearthborn.studios.ndial),
by Hearthborn Studios.

NDial itself does not record calls. This separate app does the recording on your phone; NDial only
starts and stops it from the call screen. Recordings are stored, played and managed inside this app
and never leave your device.

## Download

The latest APK is in this repository: **`NDialRecorder-<version>.apk`**, with its SHA-256 in
`NDialRecorder-<version>.apk.sha256`.

This app is not on Google Play and cannot be — the mechanism it uses is not allowed for a Play app.
It is only ever published here, by Hearthborn Studios. Do not install a copy from anywhere else.

## Requirements

- Android 12 or newer.
- NDial installed from Google Play.
- [Shizuku](https://shizuku.rikka.app/) (free, from Google Play or GitHub).
- A phone that lets call audio be captured. Not all do — see *Does it work on my phone?* below.

## Setup

1. Install NDial Recorder (the APK above). Android will ask you to allow installing from this
   source.
2. Install Shizuku and **start it**. Shizuku's own app walks you through this: enable Developer
   options, turn on Wireless debugging, and pair. A USB cable and a computer also works, with no
   Wi-Fi at all.
3. Open **NDial Recorder**. Tap **Grant access in Shizuku** and allow it in Shizuku's dialog.
4. Tap **Check this device**. The first part runs at once. The second part runs by itself during
   your next phone call — just make a call and keep talking for about fifteen seconds. The result
   arrives as a notification.
5. In NDial, open **Settings › Call Recording** to confirm the companion is detected. A **Record**
   button now appears on NDial's call screen.

**Shizuku stops when your phone restarts.** That is how Shizuku works on a phone without root, not a
fault in this app. After a restart, open Shizuku and start it again; nothing else needs to be
redone.

### Phones that limit what ADB may do

Some brands ship a Developer-options switch that quietly blocks the access Shizuku provides. If
Shizuku says it is running but the device check fails, look for these and turn them **off**:

| Brand | Setting |
|---|---|
| OnePlus / Oppo / Realme (ColorOS, OxygenOS) | *Permission monitoring* or *System optimisation* |
| Xiaomi / Redmi / POCO (MIUI, HyperOS) | turn **on** *USB debugging (Security settings)* |

The app shows the steps for your brand on its setup screen.

## Does it work on my phone?

There is no list of supported phones, on purpose: phones that block call recording usually do it by
handing over a silent stream, so the only honest answer comes from measuring your phone. That is
what **Check this device** does. A phone that fails is told so plainly.

Samsung phones block third-party call recording at the system level and will fail the check. They
have their own built-in call recording; use that instead.

## Recordings

Open NDial Recorder and tap **Recordings**. Tap a recording to play it, scrub, pause, or skip ten
seconds. Long-press, or use the buttons in the player, to share or delete it. Sharing sends a copy
to the app you choose; until you do that, a recording exists nowhere but in this app's private
storage. Uninstalling the app deletes every recording.

## Privacy

See [PRIVACY.md](PRIVACY.md). In short: recordings stay on the device, nothing is uploaded, and
NDial never receives them.

Whether recording a call is lawful, and whether the other party must be told, depends on where both
of you are. That is your responsibility. The app does not announce recording to the other party.

## Licence

Copyright © Hearthborn Studios. All rights reserved. See [LICENSE](LICENSE).
