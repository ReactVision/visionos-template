# Changelog

## v0.88.1 — 15 November 2026

Moves the template to React Native 0.88.1 and `@reactvision/react-native-visionos` 0.88.1, the line
Expo SDK 58 and `@reactvision/react-viro` 3.2.0 use. Publish it after the fork's 0.88.1.

### Changed

- **React Native 0.88.1.** `ios/`, `android/` and `tsconfig.json` follow
  `@react-native-community/template` 0.88.1: the iOS app starts from a `SceneDelegate`, Gradle and AGP
  are updated, and `tsconfig.json` no longer lists `jest` in `types`. `template/package.json` pins
  `react-native` and the `@react-native/*` packages at 0.88.1, React 19.3.0, the community CLI 20.2.0,
  TypeScript 6 and the fork at 0.88.1.
- The `visionos/` folder needs no source change for 0.88.

### Fixed

- **The visionOS Xcode project sets `XROS_DEPLOYMENT_TARGET = 26.0`.** It set none, so Xcode used the
  SDK version, and a Vision Pro on an earlier visionOS refused the app ("Requires a Newer Version of
  visionOS"). 26.0 is what the Podfile and the ViroReact podspecs already require.

## v0.86.4 — 19 September 2026

- Tracks `@reactvision/react-native-visionos` 0.86.4.
- The Xcode bundling phase points at the fork's `react-native-xcode.sh`.

## v0.86.3 — 8 September 2026

- Tracks `@reactvision/react-native-visionos` 0.86.3.
- The Podfile pins `platform :visionos, '26.0'`, the version `ViroReactUI` requires; CocoaPods refused
  the pod under the lower default.

## v0.86.x — 31 August 2026

- First release: a React Native 0.86 project whose `visionos/` folder derives from Callstack's
  `@callstack/visionos-template`, pointed at ReactVision's fork.
