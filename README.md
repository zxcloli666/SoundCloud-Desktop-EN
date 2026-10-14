<p align="center">
<a href="https://github.com/zxcloli666/SoundCloud-Desktop-EN/releases/latest">
<img src="https://raw.githubusercontent.com/zxcloli666/SoundCloud-Desktop/main/_refs/soundcloud.png" width="180px" style="border-radius: 50%;" />
</a>
</p>

<h1 align="center">SoundCloud Desktop</h1>

<p align="center">
<b>[<a href="https://github.com/okeydw/SoundCloud-Android">Android</a>] · iOS in development</b><br>
<b>Native desktop app for SoundCloud</b><br>
No ads · No captcha · No restrictions · Lightweight
</p>

<p align="center">
<a href="https://github.com/zxcloli666/SoundCloud-Desktop-EN/releases/latest">
<img src="https://img.shields.io/github/v/release/zxcloli666/SoundCloud-Desktop?style=for-the-badge&logo=github&color=FF5500&label=VERSION" alt="Version"/>
</a>
<a href="https://github.com/zxcloli666/SoundCloud-Desktop/releases">
<img src="https://img.shields.io/github/downloads/zxcloli666/SoundCloud-Desktop/total?style=for-the-badge&logo=download&color=FF5500&label=Downloads" alt="Downloads"/>
</a>
<a href="https://github.com/zxcloli666/SoundCloud-Desktop/stargazers">
<img src="https://img.shields.io/github/stars/zxcloli666/SoundCloud-Desktop?style=for-the-badge&logo=github&color=FF5500&label=Stars" alt="Stars"/>
</a>
<a href="https://github.com/zxcloli666/SoundCloud-Desktop-EN/blob/main/LICENSE">
<img src="https://img.shields.io/badge/License-MIT-FF5500?style=for-the-badge" alt="License"/>
</a>
</p>

<p align="center">
<a href="https://github.com/zxcloli666/SoundCloud-Desktop-EN/releases/latest">
<img src="https://img.shields.io/badge/Download-Latest_Release-FF5500?style=for-the-badge" alt="Download"/>
</a>
<a href="https://github.com/zxcloli666/SoundCloud-Desktop">
<img src="https://img.shields.io/badge/Source_Code-Main_Repo-0066FF?style=for-the-badge&logo=github" alt="Source Code"/>
</a>
</p>

---

![soundcloud-desktop-8.5](https://github.com/user-attachments/assets/5de1b459-34fb-4831-882b-42283f4cdc14)

---

## What is this?

**SoundCloud Desktop** is a full-featured native desktop app for listening to music on SoundCloud. Built with Tauri 2 + React 19 — it runs natively, uses minimal resources, and never lags.

Over **100,000 downloads** across Windows, Linux, and macOS.

> **Note:** Source code and development happen in the [main repository](https://github.com/zxcloli666/SoundCloud-Desktop). Codebase comments are in Russian, but the app itself supports English.

---

## Why SoundCloud Desktop

### Zero Ads

No banners, no promo inserts between tracks, no "upgrade to Pro" popups. Clean interface, just music.

### No Captcha

No endless "I'm not a robot" checks. Open the app — start listening.

### No Regional Restrictions

Full access to the entire SoundCloud catalog regardless of your location. All tracks, all artists, all genres.

### Native & Lightweight

Built with **Tauri 2** (Rust) instead of Electron:
- Installer size **~15 MB** (not 200+ MB like Electron apps)
- RAM usage **~80–120 MB** during playback
- Instant startup
- Smooth 60 FPS UI even on low-end hardware

### Multi-language

The app interface is available in **English** and **Russian**. Language is detected automatically from your system settings.

### System Integration

- **Media controls** — keyboard media keys, Windows media overlay, MPRIS on Linux
- **Discord Rich Presence** — show friends what you're listening to
- **System tray** — runs in background
- **In-app updates** — the Windows installer, macOS and AppImage builds update with an "Install and restart" button, other builds get a direct link to the right file and the exact command

---

## Download

### Windows

Go to the [releases page](https://github.com/zxcloli666/SoundCloud-Desktop-EN/releases/latest) and download:
- **`.exe`** (NSIS installer) — recommended
- **`.msi`** — alternative installer

Requirements: Windows 10 (1809+) or Windows 11

### Linux

| Format | Architecture | Best for |
|--------|-------------|----------|
| `.deb` | amd64, arm64 | Ubuntu, Debian, Mint, Pop!_OS |
| `.rpm` | amd64, arm64 | Fedora, openSUSE, CentOS |
| `.AppImage` | amd64, arm64 | Universal, runs anywhere |
| `.flatpak` | amd64 | Sandboxed |
| AUR `soundcloud-bin` | amd64, arm64 | Arch, Manjaro, EndeavourOS |

Download from the [releases page](https://github.com/zxcloli666/SoundCloud-Desktop-EN/releases/latest) or from the [website](https://soundcloud-desktop.fun/download) if GitHub does not open.

Arch and derivatives: the official [`soundcloud-bin`](https://aur.archlinux.org/packages/soundcloud-bin) package is published to the AUR automatically within a minute of every release.
```bash
yay -S soundcloud-bin
```
There is also a community package, [`soundcloud-desktop-bin`](https://aur.archlinux.org/packages/soundcloud-desktop-bin), maintained by someone else. Install only one of the two.

Install the Flatpak from our repository to get updates through `flatpak update` and app centers (GNOME Software, Discover):
```bash
flatpak install --user https://zxcloli666.github.io/SoundCloud-Desktop/flatpak/soundcloud-desktop.flatpakref
```
The downloaded `soundcloud-desktop.flatpak` connects the same repository when installed: `flatpak install --user soundcloud-desktop.flatpak`.

For AppImage:
```bash
chmod +x soundcloud-desktop-*.AppImage
./soundcloud-desktop-*.AppImage
```

### macOS

- **Apple Silicon** (M1/M2/M3/M4): `*_arm64.dmg`
- **Intel**: `*_x64.dmg`

Download from the [releases page](https://github.com/zxcloli666/SoundCloud-Desktop-EN/releases/latest). First launch: Right-click → Open.

> [!NOTE]
> **macOS blocking the launch?** The app isn't signed with an Apple Developer certificate, so Gatekeeper might show a "the app is damaged" error. It’s easily fixed with one command:
> ```bash
> xattr -cr /Applications/soundcloud-desktop.app
> ```
> After that, the app will launch normally.

---

## Updating

The app checks for new versions at startup and every six hours. To check manually and see your version, open **Settings → General → Updates**.

| Build | How it updates |
|---|---|
| Windows `setup.exe` / `.msi`, macOS `.dmg`, `.AppImage` | "Install and restart" button, settings and cache stay |
| Windows portable | Quit the app from the tray (right-click the icon, then Quit) and replace the exe with the downloaded one |
| `.deb` / `.rpm` | Install the new package over the old one |
| AUR | `yay -Syu soundcloud-bin` |
| Flatpak | `flatpak update` or your app center. Installed an older `.flatpak` and see no updates? Reinstall once with the new file: `flatpak install --user --reinstall soundcloud-desktop.flatpak` (without `--reinstall` it fails with "Directory not empty") |
| Built from source | `git pull` and rebuild |

If you installed a new version but the old one opens, the old one is still running in the tray: quit it with Quit and start the app again.

---

## Screenshots

<p align="center">

![home-screen](https://github.com/user-attachments/assets/66d6abb5-7ecd-493c-a0a1-19e7b22d2da5)

![liked-tracks](https://github.com/user-attachments/assets/d590bfe7-487b-4578-90fd-2c21646e262a)

</p>


---

## Feedback

| | |
|---|---|
| Suggest a feature | [Discussion #121](https://github.com/zxcloli666/SoundCloud-Desktop/discussions/121) |
| Report a bug | [Discussion #144](https://github.com/zxcloli666/SoundCloud-Desktop/discussions/144) |
| Star the repo | [GitHub Stars](https://github.com/zxcloli666/SoundCloud-Desktop/stargazers) — helps with visibility! |

Pull requests are welcome at the [main repository](https://github.com/zxcloli666/SoundCloud-Desktop).

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Shell | Tauri 2 (Rust) |
| Frontend | React 19, Vite 7, Tailwind CSS 4 |
| State | Zustand, TanStack Query |
| Audio | rodio (rust) |
| UI | Radix UI |
| Backend | NestJS 11, TypeORM, PostgreSQL |
| CI/CD | GitHub Actions — builds for all platforms |
| Linter | Biome |

---

## Building from Source

<details>
<summary><b>Developer instructions</b></summary>

### Requirements

- **Node.js** 22+
- **pnpm** 10+
- **Rust** 1.77+ (stable)

### Run

```bash
git clone https://github.com/zxcloli666/SoundCloud-Desktop.git
cd SoundCloud-Desktop/desktop
pnpm install
pnpm tauri dev
```

### Production build

```bash
pnpm tauri build
```

Artifacts will appear in `src-tauri/target/release/bundle/`.

</details>

---

## License

MIT. See [LICENSE](LICENSE) for details.

SoundCloud is a trademark of SoundCloud Ltd. This application is not affiliated with SoundCloud.

---

<p align="center">
<code>soundcloud desktop app</code> · <code>soundcloud desktop client</code> · <code>soundcloud for pc</code> · <code>soundcloud windows app</code> · <code>soundcloud linux</code> · <code>soundcloud macos</code> · <code>soundcloud no ads</code> · <code>soundcloud ad free</code> · <code>soundcloud no captcha</code> · <code>soundcloud player</code> · <code>soundcloud alternative client</code> · <code>soundcloud desktop download</code> · <code>download soundcloud for pc</code> · <code>soundcloud app for computer</code> · <code>soundcloud lightweight</code> · <code>soundcloud tauri</code> · <code>soundcloud native app</code> · <code>soundcloud music player desktop</code> · <code>best soundcloud client</code> · <code>soundcloud offline desktop</code>
</p>

<p align="center">
<a href="https://github.com/zxcloli666/SoundCloud-Desktop-EN/releases/latest">
<img src="https://img.shields.io/badge/Download_SoundCloud_Desktop-FF5500?style=for-the-badge&logoColor=white" alt="Download" height="50"/>
</a>
</p>
