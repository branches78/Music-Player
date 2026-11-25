# Music Player

Music Player is a basic local music player app that showcases native bit-perfect support on Android 14+.

This app was meant for personal use, but I decided to share it with anyone looking for a simple music app with native bit-perfect support.

## Main feature

The app is tailored for Android phones with native bit-perfect support, such as the Pixel 8 and later models and the Motorola Signature, which so far are the only phones reported to support it.

You can still install the app on any phone without native bit-perfect support, but the standard Android mixer will work in its place: when a DAC is connected, it resamples 44.1kHz to 48kHz and plays other sample rates directly, but not in bit-perfect mode. If the phone speaker is used, everything will be resampled to what the OS supports in that mode, usually 48kHz. As an option, you can submit a report to the website of the "[Bit-Perfect Audio Detector](https://bit-perfect-detector-web.onrender.com/)" app to contribute to its database. This way, you can help other audiophiles find out whether the phone they want to buy has native bit-perfect support by checking that website. For more info about that app, please visit its [GitHub repo](https://github.com/branches78/Bit-Perfect-Audio-Detector).

When you use this app on a supported model and connect a DAC, the app automatically switches to bit-perfect mode, ready for use, so you don't have to do anything other than start listening to your music in all its glory. The "Now playing" screen will show you if the current track is playing in bit-perfect mode. *Settings › Output mode* shows more information about the connected DAC.

You can scan any folder from your phone's internal storage, as well as shared network folders (Samba/SMB) from a computer or NAS.

The same APK also works on Android TV and Google TV devices, with its own interface made for the remote.

As I already mentioned, this app was made for personal use, so the UI is exactly the way I wanted it to be, which means I won't change it beyond the usual bug fixes and improvements.

If you have a suggestion, I may consider it depending on the request. Just open an issue and I will be more than happy to review it.

## Things I will never implement

- Bit-perfect driver support (the idea is to promote native support).
- Equalizers (by default they don't work with bit-perfect).
- ReplayGain support (by default it doesn't work with bit-perfect).
- Any other feature that modifies the original sound.

If you're looking for those, please look somewhere else. Remember, the future is native bit-perfect support.

Support for Emby, Jellyfin, Plex or any other server is not currently in my plans, but I can't say I will never implement it.

## Other features

- **Formats:** FLAC, ALAC, WAV, WavPack, MP3, AAC, Ogg Vorbis, Opus and DSD (DSF files), plus Dolby Digital, Dolby Digital Plus and Dolby Atmos in `.m4a`, and DTS in WAV, on devices that can play them.
- **Library:** artists, albums, songs, genres, composers, years, folders and M3U playlists, with sorting and search; its tabs can be hidden and reordered.
- **Playlists and favorites,** recently played and most played.
- **Lyrics:** embedded in the file, from an `.lrc` file next to the song, or from LRCLIB; synced lyrics scroll with the music. Tap the album art on the "Now Playing" screen to show them.
- **Internet radio** from the Radio Browser directory: every station with its format, including HLS (.m3u8) ones, with FLAC, nearby, country, decade and genre filters, and favorite stations.
- **Song info from MusicBrainz:** the album, year, genre and cover a song's tags lack, kept in the app without changing your files.
- **Artist photos** from MusicBrainz (Wikimedia Commons), and from Deezer when it has none.
- **Google Cast** (phone): send the music to a Chromecast, a Cast speaker or an Android TV / Google TV with Cast built in, where it shows its own "Now Playing" screen.
- **Screensaver** (TV): after a while without using the remote, an animated scene or a visualization that moves with the music covers "Now Playing".
- **Sync between devices** that use the same network folder: recently played, play counts and favorites.
- **Light, dark or system theme.**
- **Languages:** English and Spanish. If you want it in your language, please let me know.

## Installing

1. Download `MusicPlayer-1.3.0.apk` from [Releases](https://github.com/branches78/Music-Player/releases/latest).
2. Open it on the phone and allow installing apps from that source if Android asks.
3. On first launch, allow access to your files and choose your music folder.

The app is not on Google Play yet, and I still haven't decided whether I'll publish it there.

## Privacy

The app has no accounts, ads or analytics. It only connects to the internet for radio, lyrics, artist photos, song info and the bit-perfect report, if you choose to send it. Your approximate location is only used, if you allow it, to find radio stations near you. Network folder passwords are stored encrypted on the phone.

## Credits

Built with AndroidX Media3, smbj and WavPack. Radio stations from Radio Browser, song info from MusicBrainz and the Cover Art Archive, artist photos from Wikimedia Commons and Deezer, and lyrics from LRCLIB. The full list of open-source libraries and their licenses is in the app, under *Settings › About › Open-source licenses*.

The source code of this app is not public. This repository is where the app is published: download it from [Releases](https://github.com/branches78/Music-Player/releases/latest).
