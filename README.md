# LiquidClock — Redmi 12 5G

An experimental Xiaomi HyperOS theme project targeting:

- Device: Redmi 12 5G
- ROM: India (INXM)
- HyperOS: 2.0.204.0.VMWINXM
- Android: 15

## Goal

Create an iPhone-inspired Liquid Glass clock while retaining the system wallpaper and keeping lock-screen behavior as close to stock as the theme engine permits.

## Current status

This repository contains an **experimental MAML lock-screen prototype**, not a phone-tested release. The glass appearance is simulated with translucent fills, gradients and highlights. It is not true live background blur.

A custom MAML lock screen can replace parts of the stock lock screen. Notification rendering, unlock gestures, fingerprint behavior, emergency/shortcut controls and device-specific compatibility must be tested on the target phone before calling this complete. Do not install an unverified build as a daily-use theme.

## Build

GitHub Actions builds a ZIP-compatible MTZ archive from the theme directory and uploads it as an artifact. The artifact is a prototype and is not certified for HyperOS 2.0.204.0.

## Install / safety

Do not disable lock-screen security, do not grant unrelated accessibility permissions, and do not install third-party theme-installer APKs from untrusted sources. First test only after a recovery path is available (know how to switch back to the default theme).

## Project layout

- theme/description.xml — theme metadata
- theme/lockscreen/advance/manifest.xml — experimental MAML lock-screen layout
- .github/workflows/build-theme.yml — packages the theme and uploads an artifact

## References

- [MAML grammar and lock-screen documentation](https://nikiink.github.io/MAML-Grammar-en.htm)
- [HyperOS theme structure example](https://github.com/DevInfinix/IOS-Extended) (structural reference only; no proprietary assets copied)

## License

Original project files are provided under the MIT License.