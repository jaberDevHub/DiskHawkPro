# Power File Scanner (`DiskHawk Pro`)

[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20(x64)-0078D6?logo=windows)](https://github.com)
[![Engine](https://img.shields.io/badge/Engine-Native%20C%2B%2B-00599C?logo=c%2B%2B)](https://github.com)
[![Speed](https://img.shields.io/badge/Scan%20Speed-5%E2%80%938s%20%2F%204TB-brightgreen)](https://github.com)
[![Packaging](https://img.shields.io/badge/Build-Single%20File%20Standalone%20EXE-orange)](https://github.com)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> [!NOTE]
> Fast, dependency-free disk scanner for Windows. Finds the largest files and folders in **5–8 seconds**, summarizes disk usage by file type, and lists mounted drives — with a Tkinter desktop GUI (`DiskHawk Pro`) and a scriptable CLI.

---

![DiskHawk Pro Preview](diskhawk_preview.png)

---

## ⚡ What it does

| Feature | Description |
| :--- | :--- |
| **Largest files** | Rank files by size across any target folder or drive on-the-fly. |
| **Largest folders** | Recursive folder sizes so you can see exactly what's consuming space. |
| **Type / extension summary** | Disk usage grouped by file category (*Code, Document, Image, Video, Audio, Archive, Installer, etc.*). |
| **Storage Analytics** | Review 7-day, 30-day, or all-time modified activity, storage by extension, largest folders, recent files, Downloads, and installer bloat. |
| **Drive listing** | Fixed, removable, network, CD-ROM, and RAM drives with live capacity and usage stats. |
| **Open in Explorer** | Jump straight to a scanned file or folder location with one click. |
| **Reports** | Export full scan results to structured JSON or CSV (`_files`, `_folders`, `_types`). |
| **Phone over USB (GUI)** | Discovers Android storage exposed over MTP and scans files/folders without requiring a drive letter. |
| **Duplicate finder** | Three-stage verification pipeline (*Size filter → 4 KB block hash → full xxHash64*) with zero false-positives. |
| **List & grid layouts** | List view by default; Grid automatically fits items with Windows Explorer thumbnails, file icons, and video frames via FFmpeg (`Ctrl` + wheel to resize). |

---

## 🛠️ Design principles

- **Zero dependencies** — Python standard library only (`argparse`, `tkinter`, `ctypes`, `pathlib`, `heapq`, etc.). No `pip install`.
- **Production-grade scanning** — Native C++ kernel traversal (`diskhawk_fast_scanner.dll`) with multi-threaded `FindFirstFileW` (**5–8s typical drive scans, under 80 MB RAM**), heap-based top-N tracking, bounded progress reporting, and cancel support.
- **Non-blocking GUI** — Scans run on a background thread with an event queue-driven UI; window stays 100% responsive.
- **MTP access** — Windows PowerShell and Shell COM automation; scan mobile devices directly over USB.
- **PyInstaller-ready** — `resource_path()` handles onefile bundling (`sys._MEIPASS`) for `diskhawk.ico`, the embedded `diskhawk_fast_scanner.dll`, and Tkinter runtime into standalone `DiskHawkPro.exe`.

## 📋 Scope

> [!IMPORTANT]
> Local disk, mounted-volume, and GUI-based MTP phone scanning for Windows. MTP phone storage can be scanned and browsed, but phone items cannot be sent to the Windows Recycle Bin from this app. Duplicate hashing and CLI scans remain limited to normal filesystem paths.


## ❓ FAQ

**Is it free?** Yes.

**Does it phone home / send data?** No. It scans your local filesystem only.

**Does it modify files?** Only when you explicitly delete something from inside the app.

---

## 📄 License

Released under the [MIT License](LICENSE).

