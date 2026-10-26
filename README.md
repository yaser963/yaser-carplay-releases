**English** | [العربية](README.ar.md)

# Yaser CarPlay for BYD

**Yaser** is a CarPlay receiver app for **BYD DiLink** head units (wired USB and wireless).  
Install the APK on the **car**, not on the iPhone. Package id: `com.yaser.carplay`.

This repository is **public and binaries-only**. It hosts GitHub Releases that the app downloads when you check for updates in the car.

## Current release

- **[v0.2.21-yaser.4](https://github.com/yaser963/yaser-carplay-releases/releases/tag/v0.2.21-yaser.4)** — download `Yaser-v0.2.21-yaser.4.apk` from the Release page (not from the git tree).

Always use the **Releases** tab. Ignore empty branches / tree files.

## Install (first time)

1. Allow unknown apps / APK install on the BYD head unit.
2. Copy the APK onto the car (USB stick, file manager, etc.) and install it.
3. Open **Yaser** → grant Bluetooth / Wi‑Fi / microphone permissions as prompted.
4. Prefer the car’s **built-in 5 GHz hotspot** (or a known-good USB data cable).
5. On the iPhone: Bluetooth + Wi‑Fi on → pair / join → Connect in Yaser → accept CarPlay prompts.

If you previously installed `yaser.1` or `yaser.2`, uninstall that build once before installing `yaser.3` or newer (signing key changed at `.3`). From `.3` → `.4` and later, updates can install over the top.

## Updates from the car (no USB stick)

With internet on the head unit:

1. Open Yaser → **Settings → About → Check for updates**, or  
2. Enable **background update checks** in settings (optional).

The app contacts this repository’s Releases over HTTPS, downloads a newer matching APK, verifies checksum + signature, and installs it. You do not need a flash drive for later updates.

## Features

- Wired and wireless CarPlay for BYD DiLink
- Dashboard / cluster-oriented navigation helpers (turn card and related CN UI)
- Boot ADB repair and Bluetooth pause helpers (when ADB / permissions allow)
- Richer connection and display settings
- In-car update checks against this Releases feed
- Diagnostic reporting for connection issues

## Fixes in recent Yaser builds

Included in `0.2.21-yaser.4` (ported from merged DiPlay work):

- More reliable wireless Bonjour startup (avoid unnecessary reverse DNS)
- Hotspot interface detection that ignores cellular modem interfaces (`rmnet*` / `ccmni*`) common on BYD units
- Wired USB: retry CarPlay start when the phone’s USB network comes up late, with a longer start window for Save & reconnect cases

Still environment-dependent (no guaranteed fix in this APK alone): some iOS 27 wireless cases, rare USB detection vs native CarPlay, and Bluetooth call duplex conflicts when ADB is unavailable — prefer 5 GHz car hotspot and a known-good cable as fallbacks.

## Trust & security

- Install only APKs attached to **Releases** on **this** repository.
- The in-app updater refuses mismatched package ids, tag names, checksums, or signing certificates.
- This repo does not contain source. Treat random APKs from elsewhere as untrusted.

## Support scope

Yaser targets **BYD DiLink** head units. Other brands / aftermarket HUs are out of scope for this build.
