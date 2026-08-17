<div align="center">

<img src="assets/wallhex_Hegxib_logo.png" alt="WallHex" width="200" />

# WALLHEX

**Video live wallpaper for Windows**

[![Windows 10/11](https://img.shields.io/badge/Windows-10%2F11-7b2ff7?style=for-the-badge)](#requirements)
[![4K Ready](https://img.shields.io/badge/4K-Ready-00d4ff?style=for-the-badge)](#features)
[![Lightweight](https://img.shields.io/badge/Lightweight-f72585?style=for-the-badge)](#what-it-doesnt)
[![mpv Powered](https://img.shields.io/badge/mpv-Powered-00b4d8?style=for-the-badge)](#features)
[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4?style=for-the-badge)](#requirements)

</div>

---

## What it does

- Turns any video into a live Windows wallpaper, playing behind your desktop icons
- Loops the video forever, always muted
- Works with files (`.mp4`, `.webm`, `.gif`) and video URLs
- **Multi-monitor support** — same video on every screen, one stretched across all, or a different one per screen
- Auto-starts with Windows
- Adds a right-click **"Set as live wallpaper"** menu entry to every video file (Win 11 + Win 10)
- Adds a tray icon — **Exit** restores your original wallpaper

---

## Install

Just run `WallHex.exe`. On first launch it installs itself:

- ✅ Adds right-click **"Set as live wallpaper"** to video files (Win 11 + Win 10)
- ✅ Registers start-with-Windows
- ✅ Extracts its bundled mpv engine

**No other installer, no admin needed, no extra downloads.**

> **Use it:** Right-click any video → **Set as live wallpaper**
>
> **Uninstall it:** Tray icon → **Uninstall WallHex** — closes it, removes the menu entries and start-with-Windows, and restores your original wallpaper.

---

## What it doesn't

- No audio. Ever.
- No telemetry, no analytics, no tracking, no network calls on its own.
- No services, no drivers, no kernel stuff.
- Doesn't touch your files, registry, or wallpaper settings permanently — original wallpaper comes back on exit.
- Not a video player you open windows with.

---

## Features

| Feature | Details |
|---|---|
|  Hardware decoding | 4K/HDR playback via bundled mpv |
|  Desktop-icon layer injection | True wallpaper look — icons stay clickable on top |
|  Self-healing | 3-second watchdog recovers automatically after Explorer restarts or theme/display changes |
|  Fullscreen enforcement | Applied on every monitor |
|  Auto-start & single-instance | Registered at install; launching a new video swaps it live |
|  Crash resilience | Process survives shell crashes; video keeps playing |

---

##  What you expect

| Step | What happens |
|---|---|
| **Get** | A single `.exe`. No runtime downloads, no separate installer. |
| **First use** | Run it once (it installs itself), then right-click a video → *"Set as live wallpaper"* |
| **Switching** | Play another video from the menu — it replaces the current one instantly |
| **Stopping** | Tray icon → **Exit**. Wallpaper restored. |
| **Removing** | Tray icon → **Uninstall WallHex** |

>  **Warning:** Killing it via Task Manager can leave the desktop black until you change your wallpaper manually. Always use **Exit**.

### Security

Signed `CN=Hegxib, O=Hegxib` (self-signed, so "Unknown publisher" is expected). No virus history. Check the hash anytime on [VirusTotal](https://www.virustotal.com/gui/file/65449A8E6AA899FF15DE763D7EECBC8A26A74FF813C711D39D273065CDD2EA69).

```
SHA-256  65449A8E6AA899FF15DE763D7EECBC8A26A74FF813C711D39D273065CDD2EA69
```

---

## 💻 Requirements

- Windows 10 or 11, 64-bit
- .NET 10 runtime (bundled into the exe — no separate install needed)

---

## 🔨 Build

```bash
dotnet build src\WallHex -c Release
```

---

## 📄 License

No ownership. Personal/educational use only, no commercial use. See [LICENSE](LICENSE).
