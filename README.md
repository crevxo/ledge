# Lunette

A notch hub for Apple silicon Macs. Media, calendar, files, and a set of small
tools live in the notch and stay out of the way until you hover it.

## What it does

- **Now playing** with artwork, seek, volume, shuffle and repeat, synced
  lyrics, and a spectrum meter driven by real system audio.
- **Live activity** that wraps around the cutout while a track plays, the way
  the Dynamic Island does. Battery, charging and Bluetooth events surface the
  same way.
- **Calendar** for the day, with per-calendar filtering and event creation
  without leaving the notch.
- **Shelf** for files, links, and text — drop, stack, Quick Look, drag back out.
- **Tools:** timers, stopwatch, notes, to-dos, Shortcuts, camera mirror,
  clipboard history, Reminders, weather, system stats, keep awake.
- **Volume and brightness HUD** replacement, if you want it in the notch
  instead of the middle of your screen.
- Hover, click, a hotkey, or trackpad gestures to open. ⌃⌥K for the command
  palette.

Everything past the basics is off by default. Nothing runs a timer or watches
the system until you switch it on.

## Installing

Download the DMG below, open it, drag Lunette to Applications.

The app is signed but not notarized, so the first launch is blocked. Either run

    xattr -dr com.apple.quarantine /Applications/Lunette.app

or open System Settings → Privacy & Security and click **Open Anyway**. That
clears the "downloaded from the internet" flag. Worth looking the command up
rather than taking my word for it.

**Apple silicon only.** macOS 14 or later.

## Permissions

Asked for only when you turn on the feature that needs them: Calendar,
Reminders, Camera for the mirror, Bluetooth for device events, Accessibility
for the media-key HUD, and audio capture for the live waveform. Decline any of
them and the rest still works.

## Updates

Lunette checks this repository when it opens and asks before downloading or
installing anything. It verifies the published SHA-256 of the download before
it replaces the app.

## Source

The source is in a private repo. This one holds the builds.

## Credits

Lunette began from [Atoll](https://github.com/rutmehta/Atoll) by Rut Mehta,
MIT licensed. The original copyright and licence are kept in `LICENSE` here and
in the source. The media layer uses the MIT-licensed `mediaremote-adapter`.

## Bugs

Open an [issue](../../issues). This has mostly run on one Mac, so real reports
are useful — especially if the closed notch does not sit flush on yours, in
which case Settings → Appearance → Notch fit is the knob.
