# DiskHawkPro v1.0.0 — Release notes

This repository already contains the single-file Windows executable `DiskHawkPro.exe` in the repository root. That is the distributable: no installation is required — download the .exe and double-click to run.

Highlights
- Standalone Windows executable (no Python or other runtime required).
- Fast disk scanning, largest files and folders, CSV export, and quick actions.

Recommended assets to attach to the GitHub release page
- DiskHawkPro.exe (already present in the repo root — but upload the built exe to the release so GitHub serves it as a downloadable asset)
- SHA256SUMS (file with checksums for the distributed exe)
- Optional: user-manual.pdf, example-report.csv

Notes for publishing the release
1. Create tag: v1.0.0 (target: main)
2. Release title: v1.0.0 — First public release
3. Release description: paste the contents of RELEASE_BODY.md (or the short summary in this file)
4. Upload assets (DiskHawkPro.exe and SHA256SUMS) to the release before publishing

Security
- The executable is unsigned and may trigger SmartScreen or AV warnings on first run; follow the README instructions for SmartScreen "More info → Run anyway".

