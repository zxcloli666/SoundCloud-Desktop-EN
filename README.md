<p align="center">
<a href="https://github.com/zxcloli666/SoundCloud-Desktop-EN/releases/latest">
<img src="https://raw.githubusercontent.com/zxcloli666/SoundCloud-Desktop/legacy/icons/appLogo.png" width="180px" style="border-radius: 50%;" />
</a>
</p>

<h1 align="center">SoundCloud Desktop</h1>

<p align="center">
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

> [!CAUTION]
> Support project:
> 
> Boosty: https://boosty.to/lolinamide
> 
> TON: UQAiVd_p6zV3iYNy0H9ZokH6_OEvzSrk-88taa7Mc2kE7pUZ
> 
> LTC: LLw3Wh1eGDetjoCc76cbfEHusy1vvaupo8
> 
> BTC: bc1qqjk9vy453q9jxvpwm7qa4wg3fw03rgzfa9xadf
> 
> and vote - [#264](https://github.com/zxcloli666/SoundCloud-Desktop/discussions/264)

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
- **Auto-updates** — new versions install with one click

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
| `.flatpak` | amd64 | Sandboxed, auto-updates |

Download from the [releases page](https://github.com/zxcloli666/SoundCloud-Desktop-EN/releases/latest).

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
