# Release checklist — what I committed for you

I added the following files to the repository so you can publish a neat release quickly:

- CHANGELOG.md
- RELEASE_NOTES.md
- RELEASE_BODY.md

What you still need to do in the GitHub UI (two minutes):

1. Go to: https://github.com/jaberDevHub/DiskHawkPro/releases/new
2. Tag version: `v1.0.0` (create new tag)
3. Release title: `v1.0.0 — First public release`
4. Paste the contents of `RELEASE_BODY.md` into the release description.
5. Upload the executable `DiskHawkPro.exe` as a release asset (click "Attach binaries by dropping them here or selecting them").
   - Tip: select the DiskHawkPro.exe file from your local machine (do NOT upload from the repository file view). If you want the repo's copy used, download it from the repo and re-upload to the release.
6. (Optional but recommended) Create `SHA256SUMS` locally and upload it to the release. Commands to run locally (Windows PowerShell):

   - Get-FileHash -Algorithm SHA256 .\DiskHawkPro.exe | Format-List

   Copy the hash into a file called `SHA256SUMS` with a single line:

   `e3b0c44298fc1c149afbf4c8996fb924...  DiskHawkPro.exe`  (replace the hash with the computed SHA256)

7. Click "Publish release".

If you want, I can also update the `SHA256SUMS` file in the repo after you paste the actual checksum here or tell me the checksum value.

