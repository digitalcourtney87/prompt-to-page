# Prompt to Page

**Build accessible GOV.UK Design System prototypes from plain English — no code, no cloud, no account.** A free, independent beta for **macOS and Windows** that runs an AI model entirely on your own device. After model setup, generating prototypes needs no internet connection; during the beta the app sends two limited usage events by default when online — see [Privacy during the beta](#privacy-during-the-beta).

> **Prompt to Page is an independent project.** It is not affiliated with, endorsed by, or associated with the Government Digital Service (GDS), the Crown, or the UK government. "GOV.UK" and the GOV.UK Design System are referenced for descriptive purposes only.

This repository hosts the **downloads only**. By installing, you agree to the beta terms in [EULA.md](EULA.md).

## What's new in 0.3.0

**0.3.0 is the measured-quality release.** The model picker now shows measured quality for each design system a model has been evaluated on, NHS.UK is fully quality-evaluated, eight models respond faster with no measured quality loss, generation issues are surfaced in a per-page quality report, and you can edit the generated HTML directly. Also: **macOS builds are now signed and notarized by Apple — the first-launch Terminal step is gone.** The **Windows build ships the same release**, and Windows in-app updates are live: on 0.2.x, use **Settings → Updates** to move to 0.3.0 in place — no re-download needed. See the [release notes](https://github.com/digitalcourtney87/prompt-to-page/releases/latest) for the full list.

## Requirements

### macOS

- A **Mac with Apple Silicon** (M1, M2, M3, or newer)
- **macOS 14** (Sonoma) or later
- **16 GB RAM** minimum
- ~10 GB free disk space (an AI model downloads on first run)

### Windows

- **Windows 10 or 11**, 64-bit
- **16 GB RAM** minimum
- ~10 GB free disk space (an AI model downloads on first run)
- **Microsoft Edge WebView2 Runtime** — preinstalled on current Windows. If it's missing, install the free [Evergreen Runtime](https://developer.microsoft.com/microsoft-edge/webview2/).

## Download

Get the latest build for your platform from the releases page:

- **macOS:** `Prompt-to-Page_<version>_aarch64.dmg`
- **Windows:** `Prompt-to-Page_<version>_x64_en-US.msi`

### → **[Download the latest release](https://github.com/digitalcourtney87/prompt-to-page/releases/latest)**

## Install

### macOS

1. Open the downloaded `.dmg` and drag **Prompt to Page** into your **Applications** folder.
2. Open **Prompt to Page** from Applications. The app is signed and notarized by Apple, so it opens without warnings — no Terminal commands needed.

> **Upgrading from an older beta?** Releases before notarization (0.2.4 and earlier) needed a one-time Terminal command to clear the download quarantine. That step is no longer required — just replace the app in Applications with the new download. Your prompts, pages, and the model still never leave your device.

### Windows

1. Download `Prompt-to-Page_<version>_x64_en-US.msi` and double-click it to run the installer.
2. This beta is **not yet code-signed**, so Windows SmartScreen will warn *"Windows protected your PC."* This is expected. Click **More info → Run anyway** to continue.
3. Finish the installer, then launch **Prompt to Page** from the Start menu.

> On first launch the app runs a one-time setup that downloads a local AI model. Your prompts, pages, and the model never leave your device.

**Need more detail or hit a problem?** See the full [Windows install & troubleshooting guide](install-windows.md).

## Updating

- **macOS:** the app checks for updates on launch and installs new versions with your consent (toggle in Settings → Updates). To update manually, download the new `.dmg` and drag it into Applications to replace the old version — no Terminal command needed.
- **Windows:** the app checks for updates on launch and installs new versions with your consent (Settings → Updates); approve the Windows installer prompt when it appears. To update manually, download the new `.msi` and run it — it upgrades the existing installation in place.

## Privacy during the beta

Prompt to Page sends `app_started` and `app_exited` events to Aptabase by default
during the closed beta to measure aggregate use and improve the app. Aptabase
derives a daily rotating identifier from connection data and says analytics may be
stored for up to five years. Events never include prompts, generated pages, project
content, model names, file paths or persistent install/account identifiers. Turn
them off at any time in Settings → Privacy. Read the complete privacy notice at
https://prompttopage.xyz/privacy.

Your prompts, generated pages, and models stay on your device.

## Feedback

Found a bug or have a suggestion? Email **courtney.rj.allen@gmail.com**.

---

© 2026 Courtney Allen. All rights reserved. Prompt to Page is proprietary software, licensed not sold — see [EULA.md](EULA.md).
