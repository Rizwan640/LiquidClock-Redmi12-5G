# LiquidClock — Redmi 12 5G

Experimental Xiaomi MAML theme project targeting:

- Device: Redmi 12 5G
- ROM: India (INXM)
- HyperOS: 2.0.204.0.VMWINXM
- Android: 15

## Goal

Create an iPhone-inspired Liquid Glass clock while retaining the system wallpaper and keeping lock-screen behavior as close to stock as the theme engine permits.

## Current status

This repository contains an **experimental MAML lock-screen prototype**, not a phone-tested release. The glass appearance is simulated with translucent fills, gradients and highlights. It is not true live background blur.

A custom MAML lock screen can replace parts of the stock lock screen. Notification rendering, unlock gestures, fingerprint behavior, emergency/shortcut controls and device-specific compatibility must be tested on the target phone before calling this complete. Do not install an unverified build as a daily-use theme.

The manifest now includes a documented MAML slide-up `Unlocker` structure and requests the system wallpaper. This does **not** prove that HyperOS 2.0.204.0 will preserve every stock feature.

## Build

GitHub Actions:
1. Parses the XML files.
2. Checks that the MAML lock-screen manifest contains wallpaper, date/time and unlocker elements.
3. Packages the theme directory as an MTZ-compatible ZIP archive.
4. Verifies required archive entries and ZIP integrity.
5. Uploads the prototype artifact.

These are structural/package checks only. They do not run Xiaomi's Theme Editor or test the theme on a Redmi 12 5G.

## Safety

- Do not disable lock-screen security.
- Do not grant unrelated accessibility permissions.
- Do not install third-party theme-installer APKs from untrusted sources.
- Before testing, know how to switch back to the default theme.
- If unlock, notifications or emergency controls behave unexpectedly, immediately revert to the default theme.

## Project layout

- `theme/description.xml` — theme metadata
- `theme/lockscreen/advance/manifest.xml` — experimental MAML lock-screen layout
- `.github/workflows/build-theme.yml` — structural checks, packaging and artifact upload

## References

- [Xiaomi Theme Designer — Lock Screen Getting Started](https://zhuti.designer.xiaomi.com/docs/blog/LockScreenGettingStarted.html)
- [Xiaomi Theme Designer — MAML Grammar](https://zhuti.designer.xiaomi.com/docs/grammar/index.html)

## License

Original project files are provided under the MIT License.
