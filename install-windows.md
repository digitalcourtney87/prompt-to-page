# Install Prompt to Page on Windows

A step-by-step guide to installing and updating **Prompt to Page** on Windows, plus fixes for the most common problems. For the short version, see the [README](README.md).

> **Prompt to Page is an independent project.** It is not affiliated with, endorsed by, or associated with the Government Digital Service (GDS), the Crown, or the UK government.

## Requirements

- **Windows 10 or 11**, 64-bit
- **16 GB RAM** minimum
- **~10 GB free disk space** — a local AI model downloads on first run
- **Microsoft Edge WebView2 Runtime** — preinstalled on current Windows. If it's missing, install the free [Evergreen Runtime](https://developer.microsoft.com/microsoft-edge/webview2/).

## 1. Download

Get the latest Windows installer from the releases page:

### → **[Download the latest release](https://github.com/digitalcourtney87/prompt-to-page/releases/latest)**

Look for the file named `Prompt-to-Page_<version>_x64_en-US.msi` (for example, `Prompt-to-Page_0.2.5_x64_en-US.msi`).

## 2. Install

1. Double-click the downloaded `.msi` to run the installer.
2. This beta is **not yet code-signed**, so Windows SmartScreen will warn *"Windows protected your PC."* This is expected for an unsigned installer. Click **More info → Run anyway** to continue.
3. If Windows shows a **User Account Control** prompt asking to allow the app to make changes, click **Yes** — the installer writes to `C:\Program Files\Prompt to Page`.
4. Finish the installer, then launch **Prompt to Page** from the **Start menu**.

## 3. First launch

On the first launch the app runs a one-time setup that **downloads a local AI model** (a few GB — allow some time on a slower connection). After that, everything runs entirely on your device: your prompts, the pages you build, and the model never leave your computer, and no internet connection or account is required.

## Updating

Download the new `.msi` from the [releases page](https://github.com/digitalcourtney87/prompt-to-page/releases/latest) and run it — it upgrades your existing installation in place. Your downloaded model and settings are kept. The app can also prompt you when an update is available.

## Troubleshooting

### The app closes immediately / never opens

Update to **0.2.5 or later** — earlier builds had a startup crash that could close the app the moment it launched. Download the newest `.msi` from the [releases page](https://github.com/digitalcourtney87/prompt-to-page/releases/latest) and run it.

### "Windows protected your PC" (SmartScreen)

Expected — the installer isn't code-signed yet. Click **More info**, then **Run anyway**. If you don't see **More info**, your organisation may block unsigned installers; try a personal device.

### The window is blank, white, or won't render

Install or repair the **Microsoft Edge WebView2 Runtime** (the [Evergreen Runtime](https://developer.microsoft.com/microsoft-edge/webview2/)), then relaunch. Prompt to Page uses WebView2 to render its interface.

### Generation seems stuck on "warming up"

The first generation after launch loads the model into memory and can take noticeably longer than later ones, especially on machines without a discrete GPU. Give the first run a minute; subsequent generations are faster.

### Antivirus flags the installer or the helper process

Because the installer is unsigned and the app bundles a local AI engine (`llama-server.exe`) that runs as a helper process, some antivirus tools flag it heuristically. You can allow it, or verify your download against the release page.

## Feedback

Found a bug or have a suggestion? Email **courtney.rj.allen@gmail.com**.

---

© 2026 Courtney Allen. All rights reserved. Prompt to Page is proprietary software, licensed not sold — see [EULA.md](EULA.md).
