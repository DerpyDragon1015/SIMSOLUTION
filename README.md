# SimSolution

A Windows app that finds, downloads, safety-checks and installs **The Sims 4** custom content, and lets you manage it in a picture gallery.

> Unofficial fan tool. Not affiliated with or endorsed by Electronic Arts, Maxis, Patreon or CurseForge/Overwolf.

## Download

1. Download the latest `SimSolution-<version>-win64.zip` from the [Releases](../../releases) page.
2. Extract the zip. Keep the folder together, because the exe needs the files next to it.
3. Run `SimSolution.exe`. No Python install needed.

Windows may show a SmartScreen warning because the exe isn't code-signed: click **More info → Run anyway**.

SimSolution checks this page on startup and tells you when a newer version is out. It never updates itself.

## Features

- **CurseForge search**: filter by section (Create a Sim, Build/Buy, Mods, ...), category and game version, and sort by popularity, downloads, latest update and more.
- **Patreon creators**: list creators one per line and see how many posts they have, how many are downloadable and how many are members-only. Browse their content and queue everything you don't have yet with **Add all new**. Only **public/free** posts are supported; there is no login.
- **Safety checks before anything touches your Mods folder**:
  - Only Sims 4 file types are installed (`.package`, `.ts4script`, `.cfg`).
  - Files are checked by content, not just name, so renamed executables are caught.
  - Script mods (`.ts4script`) are scanned for risky code (running programs, network access, etc.) and quarantined unless you trust the creator.
  - Anything suspicious goes to a quarantine folder and is never installed.
- **Library gallery**: a picture grid of installed packs. Turn packs off or on without deleting them; disabled packs are moved out of Mods.
- Finds your Mods folder automatically (including OneDrive-redirected Documents).
- Detects duplicates, backs up any file it replaces, checks for updates, and offers to clear the game's thumbnail cache.

The safety checks reduce risk but can't guarantee a file is safe. Only install content from creators you trust.

## CurseForge API key

CurseForge search needs a free personal API key from the [CurseForge for Studios console](https://console.curseforge.com/). Enter it in **Settings**. It is stored encrypted with Windows DPAPI, tied to your Windows account. Some authors disable third-party downloads; those mods show **Open on CurseForge** instead.

## Privacy

There is no telemetry and no accounts. The app only talks to CurseForge, Patreon, file hosts you download from, and GitHub (for the update check). Errors are written to a local log file, `simsolution.log` in the app's data folder, which you can attach to an issue yourself.

## Requirements

- Windows 10 or 11 (64-bit)
- The Sims 4

`requirements.txt` lists the Python packages the exe is built with, for reference.

## License

[MIT](LICENSE)
