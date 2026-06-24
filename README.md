<div align="center">

<img src="diskhawk_preview.png" alt="DiskHawk Pro" width="128" height="128" />

# DiskHawk Pro

**Fast, dependency-free disk scanner for Windows.**

Find what's eating your disk in seconds — no install, no Python, no clutter.

[![Download](https://img.shields.io/badge/Download-DiskHawkPro.exe-2ea44f?style=for-the-badge&logo=windows)](../../releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=flat-square&logo=windows)](#)
[![Size](https://img.shields.io/badge/Size-~10%20MB-blue?style=flat-square)](#)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)

</div>

---

## ⬇️ Download

1. Go to the [**Releases**](../../releases/latest) page.
2. Download **`DiskHawkPro.exe`**.
3. Double-click to run. **No installation required.**

> **Note:** Single self-contained `.exe`. Drag it anywhere — no extra folders, no Python needed.

---

## ✨ Features

- **Largest files** — surface the biggest files of any type across a drive.
- **Largest folders** — recursive folder size ranking to find heavy directories.
- **Type/extension summary** — see which file types consume the most space.
- **Duplicate finder** — detect duplicate files to reclaim wasted space.
- **Drive listing** — fixed, removable, and network drives.
- **CSV export** — export scan results for reports or spreadsheets.
- **Quick actions** — open file/folder location in Explorer, or delete from inside the app.
- **USB / phone storage** — scans phones and external drives when mounted as a drive letter.

---

## 🚀 Usage

1. Launch `DiskHawkPro.exe`.
2. Pick a drive or folder to scan.
3. Browse largest files, largest folders, and type breakdown.
4. Right-click → open location, or export results to CSV.

---

## 🔒 Security & Antivirus

DiskHawk Pro is an unsigned independent build, so SmartScreen or some antivirus engines may show a warning on first run. This is a **false positive** common to PyInstaller `.exe` files.

To run:

1. Click **More info → Run anyway** on the SmartScreen prompt.
2. The build uses **no UPX packing** specifically to reduce false positives.

> Only download `DiskHawkPro.exe` from this repository's official [Releases](../../releases/latest).

---

## 📋 Requirements

- **OS:** Windows 10 or 11 (64-bit)
- **Runtime:** None — Python is bundled inside the executable.
- **Permissions:** Standard user. Scanning system drives may show access-denied on protected folders (skipped safely).

### Phone scanning notes

- Works when phone storage is mounted as a **drive letter**.
- Pure **MTP-only** devices that expose no drive letter are not scannable via standard filesystem APIs.

---

## ❓ FAQ

**Is it free?** Yes.

**Does it phone home / send data?** No. It scans your local filesystem only.

**Does it modify files?** Only when you explicitly delete something from inside the app.

**Why is the file ~10 MB?** It bundles the Python runtime so you don't have to install anything.

---

## 📄 License

Released under the [MIT License](LICENSE).
