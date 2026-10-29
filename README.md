**English** | [العربية](README.ar.md)

# Yaser CarPlay for BYD

**Yaser** is a CarPlay receiver app for **BYD DiLink** head units (wired USB and wireless).  
Install the APK on the **car**, not on the iPhone. Package id: `com.yaser.carplay`.

This repository is **public and binaries-only**. It hosts GitHub Releases that the app downloads when you check for updates in the car.

## Current release

- **[v0.2.22-yaser.1](https://github.com/yaser963/yaser-carplay-releases/releases/tag/v0.2.22-yaser.1)** — download `Yaser-v0.2.22-yaser.1.apk` from the Release page (not from the git tree).

Always use the **Releases** tab. Ignore empty branches / tree files.

## Install (first time)

1. Allow unknown apps / APK install on the BYD head unit.
2. Copy the APK onto the car (USB stick, file manager, etc.) and install it.
3. Open **Yaser** → grant Bluetooth / Wi‑Fi / microphone permissions as prompted.
4. Prefer the car’s **built-in 5 GHz hotspot** (or a known-good USB data cable).
5. On the iPhone: Bluetooth + Wi‑Fi on → pair / join → Connect in Yaser → accept CarPlay prompts.

If you previously installed `yaser.1` or `yaser.2`, uninstall that build once before installing `yaser.3` or newer (signing key changed at `.3`). From `.3` onward (including `0.2.22-yaser.1`), updates can install over the top.

## Updates from the car (no USB stick)

With internet on the head unit:

1. Open Yaser → **Settings → About → Check for updates**, or  
2. Enable **background update checks** in settings (optional).

The app contacts this repository’s Releases over HTTPS, downloads a newer matching APK, verifies checksum + signature, and installs it. You do not need a flash drive for later updates.

Notes:

- Android needs a **full signed APK** (not a tiny binary patch). Interrupted downloads **resume**; a verified cache skips re-download.
- Publishing a Release here is what cars see. Source pushes alone do not update the car.

## Features (0.2.22-yaser.1)

- DiPlay **0.2.22** baseline + DiPlay-CN extras
- Music clock / cluster music improvements
- Hotspot reliability improvements
- USB microphone uplink fixes
- Clearer connection failure messages
- Optional **music over car Bluetooth**, navigation/prompts/calls still on CarPlay
- Wired and wireless CarPlay for BYD DiLink
- In-car update checks against this Releases feed

## Trust & security

- Install only APKs attached to **Releases** on **this** repository.
- The in-app updater refuses mismatched package ids, tag names, checksums, or signing certificates.
- This repo does not contain source. Treat random APKs from elsewhere as untrusted.

## Support scope

Yaser targets **BYD DiLink** head units. Other brands / aftermarket HUs are out of scope for this build.
