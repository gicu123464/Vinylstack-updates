<div align="center">

# Vinylstack

### Your music, in one beautifully simple desktop player.

Search and play music, build playlists, tune the sound, and listen together — all from one place.

[**Download for Windows**](https://github.com/gicu123464/Vinylstack-updates/releases/latest) · [Features](#what-you-can-do) · [Run from source](#run-from-source)

<br>

![Windows](https://img.shields.io/badge/Windows-Ready-7257d8?style=for-the-badge&logo=windows&logoColor=white)
![Electron](https://img.shields.io/badge/Desktop-Electron-4f8b9b?style=for-the-badge&logo=electron&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-49566b?style=for-the-badge)

</div>

---

Vinylstack brings streaming, saved music, and your listening setup into a single desktop app. Find a track, build a collection, shape the sound with the equalizer, or start a shared listening room.

## What you can do

| Discover | Make it yours | Listen together |
| --- | --- | --- |
| Search and stream with yt-dlp | Save tracks and create playlists | Host or join a Listen Together room |
| Explore radio stations that keep playing | Adjust audio with the built-in equalizer | Sync playback, queue changes, and seeking |
| Import public YouTube Music playlists | Follow lyrics and control playback | Approve guests before they join |

### Built for a desktop

- A focused library with playlists, favorites, search, radio, and a queue.
- A compact player that stays available while you browse.
- Settings for downloads, audio, appearance, Listen Together, and app updates.
- Windows installer bundles yt-dlp and FFmpeg, so no separate media-tool setup is needed.
- Right-click a song to open its actions, including **Add to playlist**.
- Updates can be checked manually; automatic update downloads are off by default.

## Install on Windows

1. Download **Vinylstack-Setup.exe** from [the latest release](https://github.com/gicu123464/Vinylstack-updates/releases/latest).
2. Open the installer and follow the prompts.
3. Launch Vinylstack from the Start menu.

The release also includes **VinilStack.zip**, a source archive. The app installer and in-app update feed are both published from this repository.

## Run from source

Install [Node.js](https://nodejs.org/) 22 or later, then:

```bash
npm ci
npm start
```

For the optional local Listen Together server:

```bash
npm run listen-server
```

By default, Listen Together connects to `wss://metroserverx.meowery.eu/ws`. The address can be changed in settings. To turn off the local server bundled with the app, set `VINYLSTACK_NO_LISTEN_SERVER=1`.

## Updates

Vinylstack checks this repository’s [release feed](https://github.com/gicu123464/Vinylstack-updates/releases) for in-app updates. Open **Settings → Updates** to check for a new version, download it, and restart when prompted. Automatic update downloads are optional and disabled by default.

## Development

Pushes to `main` build the Windows installer and update metadata with GitHub Actions. The workflow downloads yt-dlp and the GPL FFmpeg build during packaging; those large executables are not stored in the source tree. To publish a new release, bump the version in `package.json` and `package-lock.json`, then push to `main`.

## License

Vinylstack source code is licensed under the MIT License. The Windows installer includes separate yt-dlp and FFmpeg executables; see their respective projects for license and source information. FFmpeg build details are included with the installed application.
