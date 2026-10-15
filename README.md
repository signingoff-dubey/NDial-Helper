# NDial Recorder

Call recording companion for [NDial](https://play.google.com/store/apps/details?id=com.hearthborn.studios.ndial),
by Hearthborn Studios.

NDial itself does not record calls. This separate app does the recording on your phone; NDial only
starts and stops it from the call screen. Recordings are stored, played and managed inside this app
and never leave your device.

## Download

**Latest: 0.1.4** — on the [Releases page](https://github.com/signingoff-dubey/NDial-Helper/releases/latest),
as `NDialRecorder-0.1.4.apk`. GitHub shows its SHA-256 next to the file.

It is a large download (about 165 MB) because the speech models for live transcription are inside
the app rather than fetched later. Nothing is downloaded behind your back, and it works with no
network at all.

The older, much smaller 0.1.0 is still in this repository as `NDialRecorder-0.1.0.apk` if you want a
build without any of the transcription work. It does not have the setup routes described below.

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
2. Install Shizuku.
3. Open **NDial Recorder**. It asks how you want to set up, and shows the steps for whichever you
   pick — see *Two ways to start Shizuku* below.
4. Once Shizuku is running, tap **Grant access in Shizuku** and allow it in Shizuku's dialog.
5. Tap **Check this device**. The first part runs at once. The second part runs by itself during
   your next phone call — just make a call and keep talking for about fifteen seconds. The result
   arrives as a notification.
6. In NDial, open **Settings › Call Recording** to confirm the companion is detected. A **Record**
   button now appears on NDial's call screen.

**Shizuku stops when your phone restarts.** That is how Shizuku works on a phone without root, not a
fault in this app. After a restart, start it again; nothing else needs to be redone.

### Two ways to start Shizuku

Recording needs a helper process running as the shell user, and on a phone without root the only
thing that hands one out is Shizuku. So Shizuku is installed either way. What differs is only how
you start it, and the app now asks which you want:

- **Shizuku** — on the phone alone. Turn on Wireless debugging, pair with the code Android shows,
  and start Shizuku from its own app. No computer, but a pairing code and a port that change every
  time.
- **ADB** — with a computer. The app lists the exact commands in order, each with a Copy button:
  `adb devices`, the command that starts Shizuku, a fallback for when Shizuku's start script is not
  there yet, and the `adb pair` / `adb connect` pair if you have no cable. The fallback command is
  built from your own phone's Shizuku folder, so it is already correct for your device.

Either way, nothing stays connected afterwards and the cable can come out.

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

## Live transcription and translation

Calls can be transcribed as they happen, and the transcript translated into another language. Both
run entirely on your phone, on models shipped inside the app — nothing is sent anywhere, and neither
needs a network connection. Choose the languages under **Live transcription** and **Live
translation** on the app's own screen, and read finished transcripts under **Transcripts**.

Accuracy varies a great deal with the language, the line quality and the accent. Treat a transcript
as a helpful record, not as a reliable one.

## Privacy

See [PRIVACY.md](PRIVACY.md). In short: recordings and transcripts stay on the device, nothing is
uploaded, and NDial never receives them.

Whether recording a call is lawful, and whether the other party must be told, depends on where both
of you are. That is your responsibility. The app does not announce recording to the other party.

## Licence

Copyright © Hearthborn Studios. All rights reserved. See [LICENSE](LICENSE).
