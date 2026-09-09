# Prompt to Page

**Build accessible GOV.UK Design System prototypes from plain English — no code, no cloud, no account.** A free, independent beta for **macOS and Windows** that runs an AI model entirely on your own device. After model setup, generating prototypes needs no internet connection; the app can send two limited usage events, but only if you switch them on — see [Privacy during the beta](#privacy-during-the-beta).

**▶ Watch it in action:** [prompttopage.xyz/demos](https://prompttopage.xyz/demos) — the full GOV.UK workflow, and the same journey on the U.S. Web Design System.

> **Prompt to Page is an independent project.** It is not affiliated with, endorsed by, or associated with the Government Digital Service (GDS), the Crown, or the UK government. "GOV.UK" and the GOV.UK Design System are referenced for descriptive purposes only.

This repository hosts the **downloads only**. By installing, you agree to the beta terms in [EULA.md](EULA.md).

## What's new in 0.5.2

A reliability release for the second and third things you ask of a page. **Version history now survives closing and reopening a project** — every load path rebuilt each page without its versions, so the trail came back empty on every reload even though the file on disk held it; Undo and the version list were only ever as long as the current session. **Regenerate and edit re-run the operation that made the page, on the page it started from**: regenerating a reply that had refined or added a section used to restore the earlier version and then regenerate the whole page, losing the section scope and rewriting content the request had never been about; both now re-run the same pipeline against the html that request started from and commit only if the page is still the one they expected, and a re-run that pauses to ask *where* resumes as a re-run rather than doubling its section. **Stop works everywhere and failures stay put** — the preview's progress overlay carries its own **Stop**, so a generation can be interrupted in distraction-free mode where the chat dock is hidden; Stop during a refinement's “which section?” turn now cancels it; and errors raise a titled banner you dismiss rather than a toast that vanishes. **Closing the window during a generation asks first**, naming what is lost — saved work is unaffected, only the unfinished result — and cancelling leaves the running model and a live LAN share in place. **“Add or change?” is one in-app sheet** instead of two native confirmations, so the three-way choice fits on one sheet and Esc reliably cancels. Fixes: Checkpoints now say when they cannot save (setup diagnostics used to grow without bound until local storage was full, at which point a new Checkpoint could not be written and the save failed with no message at all); a rejected desktop call is written to a bounded, path-redacted log instead of disappearing in a release build; and first-run copy no longer assumes a Mac. **The macOS build is available now; the Windows installer for 0.5.2 follows shortly** — install the 0.5.1 MSI meanwhile and let the app update itself. Any 0.2.x, 0.3.x, 0.4.x, 0.5.0 or 0.5.1 install can move to 0.5.2 in place via **Settings → Updates**. See the [release notes](https://github.com/digitalcourtney87/prompt-to-page/releases/latest) for the full list.

## Requirements

Hardware depends on the model you pick. **16 GB RAM is the recommended baseline, not a universal minimum** — the enabled models span **8–32 GB RAM** and about 1.1–20.4 GB per model file. The setup model picker shows what each model needs; models your machine can't run are shown greyed out under "More demanding models" rather than offered.

### macOS

- A **Mac with Apple Silicon** (M1, M2, M3, or newer)
- **macOS 14** (Sonoma) or later
- ~10 GB free disk space (an AI model downloads on first run)

### Windows

- **Windows 10 or 11**, 64-bit
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

Prompt to Page can send `app_started` and `app_exited` events to Aptabase during
the closed beta to measure aggregate use and improve the app — but **only if you
switch them on** in Settings → Privacy. They are off by default, and upgrading to
0.3.1 turns them off for everyone. Aptabase derives a daily rotating identifier
from connection data and says analytics may be stored for up to five years.
Events never include prompts, generated pages, project content, model names, file
paths or persistent install/account identifiers. Read the complete privacy notice
at https://prompttopage.xyz/privacy.

Your prompts, generated pages, and models stay on your device.

## Feedback

Found a bug or have a suggestion? Email **courtney.rj.allen@gmail.com**.

---

© 2026 Courtney Allen. All rights reserved. Prompt to Page is proprietary software, licensed not sold — see [EULA.md](EULA.md).
