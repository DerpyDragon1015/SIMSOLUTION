# SimSolution

A Windows app that finds, downloads, safety-checks and installs **The Sims 4** custom content, and lets you manage it in a picture gallery.

Made with love for my girlfriend. ❤️

> Unofficial fan tool. Not affiliated with or endorsed by Electronic Arts, Maxis, Patreon, CurseForge/Overwolf or GameTimeDev.

## Download

1. Download the latest `SimSolution-<version>-win64.zip` from the [Releases](../../releases) page.
2. Extract the zip. Keep the folder together, because the exe needs the files next to it.
3. Run `SimSolution.exe`. No Python install needed.

Windows may show a SmartScreen warning because the exe isn't code-signed: click **More info → Run anyway**.

SimSolution checks for new versions on startup. If you agree, it downloads the update, verifies it, and restarts into it. Your shortcuts follow along automatically.

## Features

- **A friendly interface with 8 colour themes**: 💎 Plumbob, 🍬 Bubblegum, 🌸 Cotton Candy, 🌙 Midnight, 🌅 Sunset, 💜 Lavender, 🌿 Mint, ☕ Llama Latte. Switch instantly in Settings.

- **Patreon creators**:
  - List creators one per line and see how many posts they have, how many are downloadable and how many are members-only.
  - Preview-only posts are hidden, and results are remembered between sessions.
  - **Add all new from <creator>** queues and starts everything you don't have yet. Mods you deleted are skipped.
  - Only **public/free** posts are supported; there is no login.
- **CurseForge search**: filter by section (Create a Sim, Build/Buy, Mods, ...), category and game version, and sort by popularity, downloads, latest update and more.
- **Install from file**: pick a `.zip`, `.7z`, `.package` or `.ts4script` you downloaded yourself. It goes through the same safety checks.
- **Safety checks before anything touches your Mods folder**:
  - Only Sims 4 content is installed: `.package`, `.ts4script`, `.cfg`, plus Gallery Tray files (lots, rooms, households), which go into your `Tray` folder.
  - Files are checked by content, not just name, so disguised programs are caught.
  - Script mods (`.ts4script`) are scanned for risky code (running programs, network access, etc.).
  - Programs and scripts (`.exe`, `.dll`, `.bat`, `.py`, ...) go to a quarantine folder and are never installed.
  - Harmless non-Sims files (readmes, images, other data) are simply left out.
- **Library gallery**:
  - A picture grid of your installed packs, with the total size of your custom content.
  - Turn packs off and on, or select several and enable, disable or delete them at once.
  - Use **Import Mods folder** to add mods you already had.
  - The **Deleted** list remembers what you removed so it's never downloaded again, and you can manage it.
- **Works alongside Sims 4 Mod Manager (S4MM)**: turning mods off uses the same `.packageOFF` / `.ts4scriptOFF` renaming, so both apps always agree on what's on or off.
- Finds your Mods folder automatically (including OneDrive-redirected Documents).
- Detects duplicates, backs up any file it replaces or deletes, checks for updates, and offers to clear the game's thumbnail cache.

The safety checks reduce risk but can't guarantee a file is safe. Only install content from creators you trust.

## CurseForge API key

CurseForge search needs a free personal API key from the [CurseForge for Studios console](https://console.curseforge.com/). Enter it in **Settings**. It is stored encrypted with Windows DPAPI, tied to your Windows account. Some authors disable third-party downloads; those mods show **Open on CurseForge** instead.

## Privacy

There is no telemetry and no accounts. The app only talks to CurseForge, Patreon, file hosts you download from, and GitHub (for the update check).

## Reporting a problem

**Please include your log file (`simsolution.log`) with every issue.** Without it, problems are very hard to track down.

Logs are in `%LOCALAPPDATA%\SimSolution\logs` (**Settings → Open log folder**): `simsolution.log` and, after a hard crash, `crash.log`. Download links are stripped of their access tokens before being written, so you can attach the logs to a GitHub issue. Check them before sharing anyway: they contain your Windows user folder paths.

## Requirements

- Windows 10 or 11 (64-bit)
- The Sims 4

`requirements.txt` lists the Python packages the exe is built with, for reference.

## License

[MIT](LICENSE)
