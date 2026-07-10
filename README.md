# Ultima II on iOS

**Play Ultima II: The Revenge of the Enchantress on your iPhone or iPad** — the complete,
original DOS game, running in DOSBox, booting straight into the game with an hourglass icon.

It's built on [dospad](https://github.com/litchie/dospad) (the open-source iOS DOSBox,
GPLv2), cloned and patched at build time, plus **your own** copy of Ultima II.

> **You must own Ultima II.** It isn't free, so **no game data is included in this repo** —
> the build copies your own copy onto the device. The DOSBox app is cloned + patched at
> build time, not re-hosted here.

## 📸 Screenshot

The real Ultima II, running in DOSBox — the app boots straight into it:

<p align="center">
  <img src="screenshots/title.png" width="440" alt="Ultima II title screen" />
</p>

## 🚀 Install

Requires a **Mac** with **Xcode** and **git**.

```sh
git clone https://github.com/dmaynard51/ultima2-ios.git
cd ultima2-ios
dosbox/build-ios-dosbox.sh ABCDE12345          # your 10-char Apple Team ID
```

It clones the iOS DOSBox, patches it to auto-run Ultima II, brands it with the hourglass
icon and the name "Ultima II", builds, signs, installs, and copies your game data onto the
device. First run: **trust the app once** under **Settings ▸ General ▸ VPN & Device
Management**, then reopen — it boots straight into the game.

By default it reads your U2 data from `/Applications/Ultima II™.app/Contents/Resources/game`
(a Mac GOG install — the **[Ultima 1+2+3 bundle](https://www.gog.com/game/ultima_123)**). If
yours is elsewhere, pass the folder (the one with `ULTIMAII.EXE`) as the last argument.

(Find your Team ID: `security find-identity -v -p codesigning` — the code in parentheses.)

## 🎮 Playing

Ultima II is keyboard-driven. dospad gives you an **on-screen keyboard** and gamepad
overlay — tap the keyboard toggle to type commands. Hold the phone in **landscape**.

## ☕ Support this port

- ☕ **[Buy me a coffee (Ko-fi)](https://ko-fi.com/dmaynard)**
- 💜 **[GitHub Sponsors](https://github.com/sponsors/dmaynard51)**

## 🙏 Credits & license

- iOS DOSBox: **[dospad](https://github.com/litchie/dospad)** by litchie (GPLv2) —
  cloned + patched at build time.
- Hourglass app icon and the build script: MIT — see [LICENSE](LICENSE).
- *Ultima II* and its data are © Origin Systems / Electronic Arts. This project ships
  none of it; you bring your own legally-owned copy.
