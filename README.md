# Aion2Rader

Recovered source: V2.1.0. V2.2 was not found and is not claimed here.

Aion2Rader-source.zip contains the original source and assets, excluding Python caches. Extract it to work on the application. No personal settings or credentials are included.

## Releases

The Windows workflow belongs at `.github/workflows/windows-release.yml`. Run it manually with the exact source version (currently 2.1.0). It builds a portable EXE ZIP, computes SHA-256, creates manifest.json, and uploads both to a **draft** release. Existing tags are not overwritten.

Before publishing, download and test on Windows: launch without Python, schedules/assets/time zones, settings persistence, update from an older EXE through the manifest, restart into the new version, and failure on a bad checksum. This workflow has not yet been run or validated.

After publishing a stable release, paste this URL in the app's Software Updates page:

https://github.com/Ilimited96/Aion2Rader/releases/latest/download/manifest.json

The URL will return 404 until a non-draft stable release includes manifest.json. The update ZIP must contain Aion2Rader.exe, not just source code. Source version and release version must match.

## Installer and uninstall

This is a portable executable, not a Windows installer. An installer with an uninstall entry remains to be implemented and tested. The current updater stages versioned folders and launches the new EXE; it does not replace an installed program or update shortcuts. No end-to-end update or uninstall claim is made.
