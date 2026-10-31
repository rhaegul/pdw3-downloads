# Project Dynasty Warriors 3

Desktop downloads published by **rhaegul**. This is an early preview of PDW3, an unofficial fan engine that builds game data locally from your own PlayStation 2 discs.

## Download

[**Open the 0.1.8 preview release**](https://github.com/rhaegul/pdw3-downloads/releases/tag/0.1.8-preview.9)

| Computer | Installer |
| --- | --- |
| Windows, x64 | [Setup EXE](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.8-preview.9/PDW3-0.1.8-preview.9-Windows-x64-setup.exe) · [MSI alternative](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.8-preview.9/PDW3-0.1.8-preview.9-Windows-x64.msi) |
| Mac, Apple Silicon (M-series) | [DMG](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.8-preview.9/PDW3-0.1.8-preview.9-macOS-AppleSilicon.dmg) |
| Linux, x64 | [AppImage](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.8-preview.9/PDW3-0.1.8-preview.9-Linux-x64.AppImage) · [Debian package](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.8-preview.9/PDW3-0.1.8-preview.9-Linux-amd64.deb) |

**This release fixes Hu Lao map verification and keeps temporary extraction files on your selected drive.** Use **Game data location → Change drive or folder** at the top of Data Loader to choose storage such as `D:\PDW3`. In 0.1.3–0.1.7, open **Settings → Check for updates**, then choose **Install and restart**. Earlier previews and Debian packages need a manual installation. Existing game data can be reused without rebuilding for this update. Python and Node are included.

Download one installer for your computer. Intel Mac builds are not included in this preview. [SHA-256 checksums](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.8-preview.9/SHA256SUMS.txt) are provided for the installers.

## What you need

- Your own **Dynasty Warriors 3 (US)** and **Dynasty Warriors 3: Xtreme Legends (US)** disc images (`.iso`). Both are required by the Data Loader.
- Optionally, your own **Dynasty Warriors 2 (US)** disc image, keeping its `.cue` and `.bin` files together.
- Optionally, your own **Warriors Orochi 2 (US)** disc image (`.iso`, SLUS_218.03).
- Plan for **at least 85 GB of free disk space** when importing all four discs. The full plan currently budgets about 76 GiB during the build and 52 GiB of output; these are conservative estimates, not measured final sizes. Use the Data Loader's estimate for your selected discs.
- Allow several hours for a full import. The additional maps and character sets increase the work; time depends on your computer and selected discs.

**No original game media comes with these downloads.** The app includes the Python and Node runtimes it needs; you do not need to install them separately. Disc files are processed on your computer.

## Install and start

1. Install the app for your computer:
   - **Mac:** open the DMG and drag the app to Applications. This preview is ad-hoc signed and is not notarized. If macOS blocks it after your first attempt to open it, follow [Apple's instructions for opening an app from an unidentified developer](https://support.apple.com/en-us/102445).
   - **Windows:** run the EXE or MSI. This preview is unsigned, so Windows may show a SmartScreen warning.
   - **Linux:** make the AppImage executable and run it, or install the `.deb` with your distribution's package installer.
2. Open **Data Loader**. Under **Game data location**, choose a folder on the drive you want to use, then choose each disc image and wait for its verification result.
3. Press **Load** for each required disc, then expand **Game data** and choose **Build game data**. Load WO2 if wanted, then rebuild after updating to add its characters. Already collected discs can be reused; the previous installation is preserved.
4. When the build finishes, return to the launcher and choose **Play Game**.

Updating from 0.1.1–0.1.7 keeps the same data folder and any game data you already imported. If updating from 0.1.0, select your disc images again and build data in the new folder; the app identifier changed in 0.1.1. Existing data is not deleted or moved.

## Change file paths or storage

In **Data Loader**, use **Change file** to replace a selected disc or find one that moved. The full path is displayed. Cancelling a picker keeps the previous selection.

Use **Game data location → Change drive or folder** to choose an empty folder on any writable drive for future loads/builds or reconnect an existing PDW3 data folder. Loaded archives, built packs and temporary extraction files use that drive. The app remembers the location after restarting or updating. **Open data folder** opens that location. Existing files are left in place; they are not copied or moved automatically. A fresh folder keeps the ISO choices but needs its game data loaded/built there.

To move existing data, copy the complete data folder and then select the copy, including `collector.json`, `collections`, `installations`, and the selection JSON files. If an external drive was unavailable when the app started, reconnect it and choose that same folder again. Finish or cancel a data operation before changing paths.

If a build failed with “Route grid does not identify the verified Hu Lao map”, update to this release and retry **Build game data**. Already collected discs can be reused. The app and updater downloads remain separate from the game-data location.

## Future updates

The app checks for updates when the launcher opens. You can also open **Settings → Check for updates**. Choose **Install and restart** when an update is available; the app verifies its signature before installing. Updates wait until imports finish. Linux in-app updates require the AppImage; update Debian packages manually.

## What to try

Open **Play Game → Free Mode** after building data. All **20 DW3**, **23 DW3XL**, and **8 DW2** battlefields are available with their required discs. DW3 includes the regular **Yellow Turban Rebellion** with Han Forces and Yellow Turbans. DW2 and XL use shared DW3 combat; events, reinforcements and some victory conditions remain incomplete. The goal is to enter the original maps and attempt their battles, not complete original-game parity.

WO2 adds **94 officers / 276 outfits**, **24 general and 47 soldier loadouts**, **238 standalone weapons**, and **370 officer weapon choices**. In Model Viewer, choose **Warriors Orochi 2** to browse them. In Free Mode, choose the **WO2** officer roster to use its officers in existing battlefields. Soldiers and alternate weapon choices are viewer content; this release does not add a playable WO2 soldier roster or WO2 maps. WO2 battle events, projectiles, effects and some combat behavior remain incomplete.

## Preview status

Release checks run the bundled disc verifier and load every importer recipe. They also check the packaged Mac app, installed Windows EXE, and importer through the actual AppImage launcher, including the required `asset_pack.py` helper. Update package signatures are verified before publication. These checks use test files, not original game media. A full fresh install and disc import on a clean machine remains untested. The Windows and Linux app interfaces have not been tested interactively. An interactive upgrade/restart from an earlier public updater-enabled release has not yet been exercised. Some stages and modes remain unfinished. On-screen controls may overlap lower menu text at some window sizes.

## Report a problem

[Open a test report](https://github.com/rhaegul/pdw3-downloads/issues/new?template=test-report.yml) with your computer model, operating system, what you tried, and what happened. If available, include the Data Loader's **Copy test report** output. Do not attach disc images or original game files.

## About this repository

This repository contains download instructions and a report template. The engine source repository is private. GitHub's automatically generated **Source code** archives contain only this download repository's documentation.

Engine code © 2026 rhaegul. All rights reserved. This is an unofficial fan project, not affiliated with or endorsed by Koei Tecmo or Sony Interactive Entertainment. Dynasty Warriors and related content belong to their respective rights holders.
