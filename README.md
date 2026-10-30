# Project Dynasty Warriors 3

Desktop downloads published by **rhaegul**. This is an early preview of PDW3, an unofficial fan engine that builds game data locally from your own PlayStation 2 discs.

## Download

[**Open the 0.1.2 preview release**](https://github.com/rhaegul/pdw3-downloads/releases/tag/0.1.2-preview.3)

| Computer | Installer |
| --- | --- |
| Windows, x64 | [Setup EXE](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.2-preview.3/PDW3-0.1.2-preview.3-Windows-x64-setup.exe) · [MSI alternative](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.2-preview.3/PDW3-0.1.2-preview.3-Windows-x64.msi) |
| Mac, Apple Silicon (M-series) | [DMG](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.2-preview.3/PDW3-0.1.2-preview.3-macOS-AppleSilicon.dmg) |
| Linux, x64 | [AppImage](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.2-preview.3/PDW3-0.1.2-preview.3-Linux-x64.AppImage) · [Debian package](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.2-preview.3/PDW3-0.1.2-preview.3-Linux-amd64.deb) |

**Windows users:** this update fixes the disc-verification startup error in the previous installer. Install 0.1.2 and choose your discs again; no separate Python installation is needed.

Download one installer for your computer. Intel Mac builds are not included in this preview. [SHA-256 checksums](https://github.com/rhaegul/pdw3-downloads/releases/download/0.1.2-preview.3/SHA256SUMS.txt) are provided for the installers.

## What you need

- Your own **Dynasty Warriors 3 (US)** and **Dynasty Warriors 3: Xtreme Legends (US)** disc images (`.iso`). Both are required by the Data Loader.
- Optionally, your own **Dynasty Warriors 2 (US)** disc image, keeping its `.cue` and `.bin` files together.
- About **40 GB of free disk space while importing**, and about **10 GB** for the finished game data. Check the Data Loader's estimate for your selected discs before building.
- Time for the first import: approximately **30 minutes to 4 hours**, depending on your computer and selected discs.

**No original game media comes with these downloads.** The app includes the Python and Node runtimes it needs; you do not need to install them separately. Disc files are processed on your computer.

## Install and start

1. Install the app for your computer:
   - **Mac:** open the DMG and drag the app to Applications. This preview is ad-hoc signed and is not notarized. If macOS blocks it after your first attempt to open it, follow [Apple's instructions for opening an app from an unidentified developer](https://support.apple.com/en-us/102445).
   - **Windows:** run the EXE or MSI. This preview is unsigned, so Windows may show a SmartScreen warning.
   - **Linux:** make the AppImage executable and run it, or install the `.deb` with your distribution's package installer.
2. Open **Data Loader**, choose each disc image, and wait for its verification result.
3. Press **Load** for each required disc, then expand **Game data** and choose **Build game data**.
4. When the build finishes, return to the launcher and choose **Play Game**.

Updating from 0.1.1 keeps the same data folder and any game data you already imported. If updating from 0.1.0, select your disc images again and build data in the new folder; the app identifier changed in 0.1.1. Existing data is not deleted or moved.

## What to try

Try **Hu Lao Gate**, **DW3 Free Mode stages 02–19**, and the **XL Yellow Turban** stage. DW3 Yellow Turban, the other XL stages, and DW2 stages are not yet importable.

## Preview status

This patch repairs the Python runtime bundled with Windows. Release builds now run the disc verifier using the bundled Python on each platform, and the Windows job also installs the EXE and checks the installed verifier. These checks use an empty test file, not original game media. A full fresh install and disc import on a clean machine remains untested. The Windows and Linux app interfaces have not been tested interactively. Some stages and modes remain unfinished. On-screen controls may overlap lower menu text at some window sizes.

## Report a problem

[Open a test report](https://github.com/rhaegul/pdw3-downloads/issues/new?template=test-report.yml) with your computer model, operating system, what you tried, and what happened. If available, include the Data Loader's **Copy test report** output. Do not attach disc images or original game files.

## About this repository

This repository contains download instructions and a report template. The engine source repository is private. GitHub's automatically generated **Source code** archives contain only this download repository's documentation.

Engine code © 2026 rhaegul. All rights reserved. This is an unofficial fan project, not affiliated with or endorsed by Koei Tecmo or Sony Interactive Entertainment. Dynasty Warriors and related content belong to their respective rights holders.
