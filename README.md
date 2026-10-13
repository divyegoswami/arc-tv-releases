# Arc TV downloads

Builds and update feeds for **Arc TV** on Mac, Android and iPhone/iPad. The Mac app is the main app; Android and iPhone are in early access. The app itself lives in a private repository; this
one only holds what the apps need to update themselves.

Arc TV is a free player for the live TV, movies and series from your own IPTV provider. It does not include any channels
or playlists.

## Arc TV 2.0

Arc TV 2.0 helps you find something to watch, and makes your data safe to move between devices.

- **Browse by genre (Mac, iPhone, iPad and Android).** Filter your matched movies and series by genre. The Mac also filters
  by decade, rating and language.
- **Library index (optional, Mac, iPhone, iPad and Android).** Genres, year and rating for your titles, fetched with your
  own TMDB key and kept only on the device it was built on. It powers Browse; on the Mac it also powers better Home suggestions.
- **Backup and restore.** One backup file works on Mac, Android and iPhone. Passwords and your TMDB key are included only
  if you tick the option, and are sealed with a passphrase you choose.
- **Sync between your devices (optional).** Your Macs, iPhone and Android phone can keep watch history, favourites and portals
  in step through a folder in your own iCloud Drive, Google Drive or Dropbox. Off until you set it up in **Settings → Sync**.
  Phones sync while Arc TV is open, and they sync movie positions only.
- **Mac extras.** Media keys and Control Center, a simpler first screen, and a Retry button when a list cannot load.
- **Android and iPhone.** Up Next, a sleep timer, mark as watched, a channel schedule, an adult-content PIN and
  screen-reader support.

Nothing is lost when you update, backups from earlier versions still restore, and the new optional features are off until
you turn them on. The match decisions switch is Mac only. The full list is in the notes of each
[release](../../releases).

## Download

| Platform | Download | Needs |
| --- | --- | --- |
| **Mac, Apple silicon** | `arc-tv-<version>-mac-arm64.dmg` from [Releases](../../releases) | macOS 12 or newer |
| **Mac, Intel** | `arc-tv-<version>-mac-x64.dmg` from [Releases](../../releases) | macOS 12 or newer |
| **Android (early access)** | `arc-tv-android-<version>.apk` from [Releases](../../releases) | Android 8.0 or newer |
| **iPhone and iPad (early access)** | Add the source below in [SideStore](https://sidestore.io) or AltStore | iOS 18 or newer |

Releases are tagged by platform: Mac `v<version>`, Android `android-<version>`, iPhone `ios-<version>`. The release marked
**Latest** is the Mac app. Every file lists its SHA-256 in the release notes.

### Mac

Open the `.dmg` and drag **Arc TV** to Applications. The app isn't notarized by Apple, so if macOS says it is damaged,
right-click it and choose **Open**. After that it updates itself: **Settings → About and data** finds the update, then
choose **Download** and **Restart to update**. Arc TV must be in your Applications folder to update itself.

### Android

Open the `.apk` and allow installs from this source when Android asks. After that the app updates itself:
**Settings → About & updates**. An update installs over the current version and keeps your data.

### iPhone and iPad (SideStore)

The app is unsigned; [SideStore](https://sidestore.io) signs it with your own Apple ID and keeps it up to date. For a
step-by-step walk-through, see the [iPhone install guide](https://divyegoswami.github.io/arc-tv-releases/iphone/).

1. In SideStore, open **Sources** and add this address:

   ```
   https://raw.githubusercontent.com/divyegoswami/arc-tv-releases/main/source.json
   ```

   (Or open Arc TV, then **Settings → About & updates → Add Arc TV to SideStore**.)
2. Install **Arc TV** from the source. iOS 18 or newer.

To update, open SideStore and refresh Arc TV. Arc TV also tells you when a new version is out (**Open SideStore to
Update**). With a free Apple ID, SideStore has to refresh the app every 7 days. Your data is kept when SideStore updates
the app.

## Privacy and credits

Arc TV has no account, no tracking and no ads. Your portals, history and settings stay on your devices. TMDB lookups and
the library index are off until you turn them on and add your own TMDB key.

This product uses the TMDB API but is not endorsed or certified by TMDB.

## Questions and problems

Open an [issue](../../issues) and say which platform and Arc TV version you use (Mac: **Settings → About and data**,
Android and iPhone: **Settings → About & updates**). Please do not post your portal address, MAC address, passwords or TMDB
key. Nothing in this repository needs them.

## What is in this repository

| File | Used by |
| --- | --- |
| `source.json` | SideStore / AltStore: the list of iOS builds |
| `android.json` | The Android app's "Check for updates" |
| `desktop.json` | The Mac app's updater |
| `icon.png` | The app icon shown in SideStore |
| `iphone/` | The [iPhone install guide](https://divyegoswami.github.io/arc-tv-releases/iphone/) (GitHub Pages) |
| Releases | The `.dmg`, `.apk` and `.ipa` files, each with its SHA-256 |

Released under the MIT licence. Made by [Divye Goswami](https://github.com/divyegoswami).
