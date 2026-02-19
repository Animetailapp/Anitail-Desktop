<div align="center">
  <img src="https://raw.githubusercontent.com/Animetailapp/AniTail/master/fastlane/metadata/android/en-US/images/icon.png" width="152" alt="AniTail Desktop logo" />
  <h1>AniTail Desktop</h1>
  <p>Native YouTube Music desktop client for Windows, macOS and Linux.</p>

  <p>
    <a href="https://github.com/Animetailapp/Anitail-Desktop/releases/latest">
      <img src="https://img.shields.io/github/v/release/Animetailapp/Anitail-Desktop?style=for-the-badge" alt="Latest release">
    </a>
    <a href="https://github.com/Animetailapp/Anitail-Desktop/releases">
      <img src="https://img.shields.io/github/downloads/Animetailapp/Anitail-Desktop/total?style=for-the-badge" alt="Downloads">
    </a>
    <a href="https://github.com/Animetailapp/Anitail-Desktop/main/LICENSE">
      <img src="https://img.shields.io/github/license/Animetailapp/Anitail-Desktop?style=for-the-badge" alt="License">
    </a>
  </p>
</div>

## Why AniTail Desktop

AniTail Desktop brings YouTube Music to desktop with a native UI, local downloads, deep playback controls, account integrations, and first-class update/backup workflows.

## Features

- Native Compose Desktop interface with fast navigation
- Playback via VLC engine for better stream compatibility
- Songs, artists, albums, playlists, charts, and explore pages
- Search, queue controls, mini player, and full player experience
- Local downloads for offline listening
- Lyrics from multiple providers with configurable priority and styling
- YouTube account login and library sync (liked tracks + playlists)
- Last.fm support (now playing + scrobbling)
- Spotify playlist import
- Discord profile/avatar integration
- Proxy support (`HTTP` / `SOCKS`)
- Backup/restore with optional Google Drive sync
- Built-in updater linked to GitHub Releases

## Download

<div align="center">
  <a href="https://github.com/Animetailapp/Anitail-Desktop/releases/latest">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-2ea043?style=for-the-badge&logo=github" alt="Download latest release">
  </a>
</div>

Published package formats:

- `windows-x64.msi`
- `windows-arm64.msi`
- `macos-arm64.dmg`
- `linux-x64.deb`
- `linux-x64.rpm`

> [!WARNING]
> If YouTube Music is not available in your region, playback may require a proxy or VPN.
>  
> `VLC Media Player` must be installed on the system for native playback.

## Build From Source

Requirements:

- Java 21
- VLC Media Player

Run the app:

```bash
./gradlew runDesktop
# or
./gradlew :desktop:run
```

Build for current OS:

```bash
./gradlew packageDistributionForCurrentOS
```

Build specific installers:

```bash
./gradlew :desktop:packageReleaseMsi
./gradlew :desktop:packageReleaseDmg
./gradlew :desktop:packageReleaseDeb
./gradlew :desktop:packageReleaseRpm
```

Artifacts:

- `desktop/build/compose/binaries/`

## Auto Update

- Source: `https://github.com/Animetailapp/Anitail-Desktop/releases/latest`
- Frequency: daily, weekly, monthly, never
- Platform-aware installer selection
- In-app download and installer launch

## Local Data Paths

```text
~/.anitail
~/.anitail/downloads.json
~/.anitail/credentials.json
~/.anitail/preferences.json
~/.anitail/database
~/Music/Anitail
~/Downloads/AniTail/AutoBackup
```

## Security

- Sensitive values are stored encrypted
- Windows: DPAPI
- Other OSes: AES-GCM local encrypted storage

## Optional Google Drive Backup

To enable Google Drive backup sync, provide one of:

- `ANITAIL_GOOGLE_CLIENT_SECRET` (env var with path to OAuth JSON)
- `client_secret.json`
- `client_secret_*.json` in project root

## License

GNU GPL v3. See `LICENSE`.

## Disclaimer

This project is independent and is not affiliated with or endorsed by YouTube or Google LLC.
