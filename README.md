# Aion2Rader

Windows companion for AION 2 Elyos events and world bosses.

## Download and update

Download the latest tested Setup EXE from [Releases](https://github.com/Ilimited96/Aion2Rader/releases). The source ZIP is for development, not installation. Releases appear only after the Windows build and installer checks pass.

In the app, open Updates > Check for updates. The update feed is:

https://github.com/Ilimited96/Aion2Rader/releases/latest/download/release.json

## Version 2.3

Refined page layouts, compact floating overlay with independent background transparency, and in-app boss maps with direct selection for 36 Elyos bosses. Skull markers are larger and have wider click targets. Existing settings, favorites and kill timers are retained.

Maps require internet access and Microsoft Edge WebView2 Runtime. Map data is provided by MetaBot.gg. Boss respawn timers use manually recorded kills and remain estimates.

## Source and validation

Extract Aion2Rader-V2.3-source.zip. Previous source archives remain available. The installed entry point is app.py; command_layout.py runs an isolated design preview.

The Windows V2.3 installer workflow checks logic, updater integrity, redesigned tabs, compiled-app launch, embedded WebView2 rendering, overlay opacity, installer handoff, settings retention and uninstall. The helper reinstall test uses the same version; a future-version download and confirmation through the full GUI is not part of the automated checks. Builds are unsigned.

Windows uninstall keeps settings by default. The app offers an explicit option to remove them. No GitHub access token or personal preview settings are embedded in the application.
