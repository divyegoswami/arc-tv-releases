# Arc TV downloads

Builds and update feeds for **Arc TV** on Android and iPhone/iPad. The app itself lives in a private repository; this
one only holds what the apps need to update themselves.

Arc TV is a free player for the live TV, movies and series from your own IPTV provider. It does not include any channels
or playlists.

## Android

Download the latest `.apk` from [Releases](../../releases), open it and allow installs from this source when Android asks
(Android 8.0 or newer). After that the app updates itself: **Settings → Updates**.

## iPhone and iPad (SideStore)

The app is unsigned; [SideStore](https://sidestore.io) signs it with your own Apple ID and keeps it up to date.

1. In SideStore, open **Sources** and add this address:

   ```
   https://raw.githubusercontent.com/divyegoswami/arc-tv-releases/main/source.json
   ```

   (Or open Arc TV, then **Settings → Updates → Add Arc TV to SideStore**.)
2. Install **Arc TV** from the source. iOS 18 or newer.

## What is in this repository

| File | Used by |
| --- | --- |
| `source.json` | SideStore / AltStore: the list of iOS builds |
| `android.json` | The Android app's "Check for updates" |
| `icon.png` | The app icon shown in SideStore |
| Releases | The `.apk` and `.ipa` files, each with its SHA-256 |

Released under the MIT licence. Made by [Divye Goswami](https://github.com/divyegoswami).
