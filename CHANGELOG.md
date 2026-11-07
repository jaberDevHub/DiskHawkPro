# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).


## [2.0.0] - 2026-11-03

### Added
- **Native C++ Acceleration:** Integrated  with Win32 kernel directory traversal, reducing 4 TB scan time from 60+ seconds to **5–8 seconds**.
- **MTP Portable Device Scanning:** Deep scan Android phones and USB media directly through Windows Shell COM without drive letter mapping.
- **Shell Thumbnail Factory:** Hardware-assisted file thumbnail previews via `SHCreateItemFromParsingName` and GDI+.
- **System Icon Support:** Native high-resolution file-type icons via `SHGetFileInfoW`.
- **Video Previews:** Automatic video frame thumbnail extraction via FFmpeg auto-detection.
- **Three-Tier Duplicate Finder:** Instant size filtering, 4 KB block header hashing, and multi-threaded full xxHash64 verification.
- **Interactive UI Tree & Search:** Visual tree navigation, instant extension filtering (`*.mp4`, `*.zip`), and direct Explorer reveal.

### Changed
- **Memory Footprint:** Drastically reduced from 150–200 MB down to under 80 MB on multi-terabyte scans.
- **Packaging:** Self-contained single-file binary (`DiskHawkPro.exe`, 10.94 MB) bundling C++ DLL and Tcl/Tk runtime.

## [1.0.0] - 2026-08-01

### Added
- First public release.
- Single-file Windows executable (`DiskHawkPro.exe`) — no install required.
- Fast recursive disk scanner with largest-files and largest-folders views.
- Extension summary, initial duplicate detection, and CSV export.

