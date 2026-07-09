# 🛠️ Tally Master Tools — Updates

[![Latest Release](https://img.shields.io/github/v/release/santoshsutar13-bot/Tally-Master-Tools-Updates?style=for-the-badge&color=05c46b&label=Latest%20Version)](https://github.com/santoshsutar13-bot/Tally-Master-Tools-Updates/releases/latest)
[![GitHub Pages](https://img.shields.io/badge/Update%20API-Live-blue?style=for-the-badge&logo=githubpages)](https://santoshsutar13-bot.github.io/Tally-Master-Tools-Updates/version.json)
[![Downloads](https://img.shields.io/github/downloads/santoshsutar13-bot/Tally-Master-Tools-Updates/total?style=for-the-badge&color=f39c12&label=Downloads)](https://github.com/santoshsutar13-bot/Tally-Master-Tools-Updates/releases)

---

## 📋 About

This repository is the **official update distribution hub** for **Tally Master Tools** — a professional all-in-one accounting utility suite built for Tally ERP / Tally Prime users.

It serves two purposes:

1. **📦 Installer Hosting** — Each release contains the latest `Tally-Master-Tools_Setup.exe` installer, ready to download and install.
2. **🔄 Auto-Update API** — The [`version.json`](https://santoshsutar13-bot.github.io/Tally-Master-Tools-Updates/version.json) file is served via GitHub Pages and acts as the update check endpoint for the application's built-in auto-updater.

---

## 🔄 How Auto-Updates Work

```
┌──────────────────────┐       HTTPS GET         ┌─────────────────────────────┐
│  Tally Master Tools  │ ──────────────────────►  │  GitHub Pages (version.json)│
│  (Client Application)│                          │  santoshsutar13-bot.github.io│
└──────────────────────┘                          └─────────────────────────────┘
         │                                                     │
         │  Compares local version                             │
         │  with latest_version                                │
         ▼                                                     │
   ┌───────────┐   If update available    ┌────────────────────┘
   │ Up to date│◄── No ── Compare ── Yes ─►│ Download Setup.exe
   └───────────┘          versions         │ from GitHub Releases
                                           └────────────────────┘
```

1. The application checks [`version.json`](https://santoshsutar13-bot.github.io/Tally-Master-Tools-Updates/version.json) on startup.
2. If `latest_version` is newer than the installed version, the user is prompted to update.
3. The installer is downloaded directly from **GitHub Releases** using the `download_url` in the JSON.
4. The update is installed seamlessly via Inno Setup's silent upgrade mechanism.

---

## 📄 version.json Structure

```json
{
  "latest_version": "40.0.5",
  "release_date": "2026-07-10",
  "download_url": "https://github.com/santoshsutar13-bot/Tally-Master-Tools-Updates/releases/download/v40.0.5/Tally-Master-Tools_Setup.exe",
  "changelog": [
    "Bug fixes and performance improvements."
  ]
}
```

| Field | Description |
|---|---|
| `latest_version` | The latest stable version number |
| `release_date` | Date of the latest release (YYYY-MM-DD) |
| `download_url` | Direct download link to the installer `.exe` from GitHub Releases |
| `changelog` | List of changes/improvements in the latest release |

---

## 📥 Download & Install

1. Go to the [**Latest Release**](https://github.com/santoshsutar13-bot/Tally-Master-Tools-Updates/releases/latest) page.
2. Download **`Tally-Master-Tools_Setup.exe`**.
3. Run the installer and follow the setup wizard.

> **System Requirements:** Windows 10/11 (64-bit)

---

## 🏗️ CI/CD Pipeline

This repository is automatically updated by the **SS Tools CI/CD Automated Pipeline**:

- ✅ Version number auto-incremented on each build
- ✅ Executable compiled via PyInstaller / Nuitka
- ✅ Installer packaged with Inno Setup
- ✅ Installer uploaded to GitHub Releases
- ✅ `version.json` metadata pushed to GitHub Pages

All deployment steps are fully automated — no manual intervention required.

---

## 👨‍💻 Developer

**Santosh Sutar** — [S S Tech Solutions](mailto:santoshsutar13@gmail.com)

📞 +91-9021323434

---

> ⚠️ **Note:** This repository is used exclusively for software distribution. The source code for Tally Master Tools is maintained in a private repository.
