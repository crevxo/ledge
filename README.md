# Ledge

The Dynamic Island, for the notch on Apple silicon Macs. Music and whatever
else is going on show up in the notch, and hovering it expands whatever it is
showing.

## What it does

- **Now playing** in the notch while a track plays: artwork on one side, a
  waveform on the other. Hover for the full player with seek, volume, shuffle,
  repeat, synced lyrics, and a waveform driven by real system audio.
- **Calls and recordings.** When an app uses the microphone or camera, the
  notch shows which one and for how long, in the same orange and green as the
  system privacy dots.
- **Downloads and AirDrop** with a progress ring, and a short "Downloaded"
  when they finish. Hover for file sizes and Show in Finder. Safari, Finder
  copies and AirDrop report progress; Chrome does not, so its downloads are not
  shown.
- **Two at once.** The more important activity takes the notch and the other
  becomes a small circle beside it. Click the circle to swap them.
- **Alerts** that take the notch over for a moment: track changes, charging,
  low battery and Low Power Mode, AirPods and other Bluetooth devices
  connecting (with AirPods battery levels), and Caps Lock.
- **Volume and brightness** in the notch instead of the middle of the screen,
  if you want it.

Every activity can be turned off separately in Settings → Live Activities.

## Installing

Download the DMG below, open it, drag Ledge to Applications.

The app is signed but not notarized, so the first launch is blocked. Either run

    xattr -dr com.apple.quarantine /Applications/Ledge.app

or open System Settings → Privacy & Security and click **Open Anyway**. That
clears the "downloaded from the internet" flag. Worth looking the command up
rather than taking my word for it.

Universal build, macOS 14 or later. Only tested on Apple silicon.

## Permissions

Asked for only when a feature needs them: Accessibility for the media keys and
Caps Lock, audio capture for the live waveform, Automation for Spotify and
Music, Bluetooth for device alerts, and your Downloads folder for the cover art
inside local music files. Decline any of them and the rest still works.

Microphone and camera activity needs no permission. Ledge only reads whether an
app is recording, the same information that drives the system privacy dots, and
never the audio or video itself.

## Updates

Ledge checks this repository when it opens and asks before downloading or
installing anything. It verifies the published SHA-256 of the download before
it replaces the app.

## Source

The source is in a private repo. This one holds the builds.

## Credits

Ledge began from [Atoll](https://github.com/rutmehta/Atoll) by Rut Mehta,
MIT licensed. The original copyright and licence are kept in `LICENSE` here and
in the source. The media layer uses the MIT-licensed `mediaremote-adapter`.

## Bugs

Open an [issue](../../issues). This has mostly run on one Mac, so real reports
are useful — especially if the closed notch does not sit flush on yours, in
which case Settings → Appearance → Notch fit is the knob.
