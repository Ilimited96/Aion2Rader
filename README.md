# Aion2Rader V2.2

The V2.2 source is preserved in `Aion2Rader-V2.2-source.zip`. Extract its `Aion2Rader` folder to work on the application. The older V2.1 archive remains available.

## Windows download

Use the Setup EXE from [Releases](https://github.com/Ilimited96/Aion2Rader/releases) once published. The source ZIP is not an installer. The installer build is currently being validated; no release is ready until the Windows workflow succeeds.

## Updates

New V2.2 installations default to this repository's update feed:

https://github.com/Ilimited96/Aion2Rader/releases/latest/download/release.json

Existing saved update sources are preserved. If an older source is saved, replace it in the app's Updates page. This feed requires a published stable release containing both `release.json` and its matching Setup EXE. V2.1's ZIP manifest format is different; install V2.2 Setup once to move to installer updates.

## Build and validation

Run the Windows V2.2 installer workflow manually in Actions. It extracts the V2.2 source archive, runs logic and updater tests, builds the EXE and Inno Setup installer, tests install/launch/update handoff/settings preservation/uninstall on a fresh Windows runner, and creates a draft release. Build outputs are unsigned.

The installer test exercises a same-version reinstall through the updater helper. A full future-version download and confirmation through the app UI still needs testing. Standard uninstall keeps user settings; the app offers separate data-removal choices.

For future versions, update source/version and the workflow's version references, replace the archive, and build a new draft. Publish only the matching installer and generated release.json together after validation. No external GitHub access token is embedded in the app; the workflow uses GitHub's temporary repository token.
