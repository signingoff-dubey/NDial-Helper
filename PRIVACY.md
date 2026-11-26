# NDial Recorder — Privacy Policy

Last updated: 20 September 2026
Publisher: Hearthborn Studios

---

## What this app does

NDial Recorder records phone calls on your device, at your request, when you tap record in NDial. It
is a separate app from NDial and does one thing.

## What it records, and where that goes

- **Call audio, only while you are recording it.** Recording never starts on its own. It starts when
  you tap record during a call, and stops when you tap stop or the call ends.
- **Recordings are stored on your device only**, in this app's private storage. They are **not**
  uploaded, not backed up to any server of ours, not shared with third parties, and not used to train
  anything.
- **NDial can play your recordings, but does not keep them.** NDial's Recorded Calls screen lists
  your recordings and transcripts and plays them by reading them from this app, through a connection
  only the genuine, signed NDial app can open (every request is checked against NDial's signing
  certificate). No file path is shared, and NDial keeps no copy.
- **We cannot read your recordings.** They never leave the device.
- **No backups or device transfers.** Recordings, transcripts and everything below are excluded from
  Android's cloud backup and from the copy a new phone offers to make during setup.

## NDial's own files kept here

Since version 0.1.7 this app also keeps a copy of some of **NDial's own** files, so they are not lost
if NDial is uninstalled and installed again: the video and voice call recordings NDial makes itself,
voicemails NDial received, and the AI summaries of your transcripts. They are stored in this app's
private storage under the same rules as the recordings, only NDial can read or delete them, and NDial
deletes its copy here whenever you delete the item in NDial. Uninstalling this app removes them.

## Transcription and translation

- **Transcribing a call turns its audio into text on your device.** The speech models are inside the
  app; no audio and no text is sent to any server, ours or anyone else's, and it works with no
  network connection at all.
- **Translation works the same way**, on downloaded language models that run on the device.
- **Transcripts are stored on your device only**, in this app's private storage, alongside the
  recordings and under the same rules: not uploaded, not backed up to any server of ours, not shared,
  not used to train anything. NDial can show them, read from this app the same way as recordings.
- Delete a transcript in the app; uninstalling removes every transcript along with every recording.

## Deleting recordings

Delete individual recordings inside the app. Uninstalling the app removes all of them, permanently
and immediately — there is no copy anywhere else.

## What leaves your device

One thing: an **access token check**. When NDial asks this app to record, it passes a short-lived
token issued by NDial's backend, which this app verifies on-device using a key built into the app.
Verifying the token does not send anything anywhere — no audio, no phone numbers, no contact
information, no call metadata.

## What this app can see, and what it does not keep

- **Microphone / call audio access**, used only for the recording you asked for and for a short test
  recording when you run the device check.
- **Notifications**, to tell you the result of the device check.
- **Speech models** shipped inside the app, used on-device to transcribe and translate. They send
  nothing anywhere.
- **Phone state**, to know when a call is active.
- This app does **not** read your contacts, your call log, or your messages. It does not know who you
  are calling, and does not write phone numbers into recording filenames or anywhere else.

## Shizuku

Recording requires [Shizuku](https://shizuku.rikka.app/), a separate third-party app you install and
run yourself. Shizuku is not operated by Hearthborn Studios and has its own terms and privacy policy.
This app uses it only to run its own recording code with the access Android requires; it sends
Shizuku no personal data.

## Your responsibility

**Laws about recording calls differ, and in many places recording without telling the other person
is illegal.** Some jurisdictions require every party to consent. Whether you may record a given call,
and whether you must announce it, is your responsibility and not something this app decides for you.
This app does not announce recording to the other party.

## Children

This app is not directed at children under 13 and we do not knowingly collect data from them.

## Changes

This policy may be updated. The date at the top reflects the current version.

## Contact

hearthbornstudio@gmail.com
