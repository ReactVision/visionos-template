<p align="center" style="background-colour: #CCCCCC;">
  <a href="https://www.reactvision.xyz/">
    <img src="https://avatars.githubusercontent.com/u/74572641?s=200&v=4" alt="ReactVision logo" width="120px" height="120px">
  </a>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/@reactvision/visionos-template">
    <img src="https://img.shields.io/npm/v/@reactvision/visionos-template" alt="npm version">
  </a>
  <a href="https://github.com/ReactVision/visionos-template/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="MIT licensed">
  </a>
  <a href="https://discord.gg/yqqEGUjK">
    <img src="https://img.shields.io/discord/774471080713781259?label=Discord" alt="Discord">
  </a>
</p>

# visionOS Project Template, By ReactVision

The React Native community template with a `visionos/` folder added, so a new project targets
iOS, Android and Apple Vision Pro from the same JavaScript.

```bash
npx @react-native-community/cli@latest init MyApp \
  --template @reactvision/visionos-template
```

That gives you `android/`, `ios/` and `visionos/`, with
[`@reactvision/react-native-visionos`](https://github.com/ReactVision/react-native-visionos)
already in `package.json`.

```bash
cd MyApp/visionos && pod install
npx react-native run-visionos
```

## Adding it to a project you already have

The template only matters when creating a project. To add `visionos/` to an existing app, generate
one into a scratch directory and copy the folder across:

```bash
npx @react-native-community/cli@latest init MyApp \
  --template @reactvision/visionos-template \
  --directory visionos-scratch --skip-install
```

## Versions

The template version tracks React Native, and the `visionos/` folder is built for that same
version. Mixing them is the thing to avoid: a `visionos/` folder from one React Native version
against another needs manual reconciliation, and that reconciliation is exactly what this package
exists to spare you.

| Template | React Native |
| --- | --- |
| `@reactvision/visionos-template@0.86.x` | 0.86.x |

## Using it with ViroReact

For 3D, AR or VR content rather than 2D UI, add [ViroReact](https://github.com/ReactVision/viro)
on top. Its config plugin does the visionOS wiring — pods, the Metro resolver, the immersive space
scene, the Xcode bundling phase — against the folder this template generates.

## Attribution

- The base is [`@react-native-community/template`](https://github.com/react-native-community/template),
  maintained by the React Native community.
- The `visionos/` folder derives from Callstack's
  [`@callstack/visionos-template`](https://github.com/callstack/react-native-visionos), updated to
  React Native 0.86 and pointed at ReactVision's fork.

## Community

<a href="https://discord.gg/A6TaFNqwVc">
  <img src="https://discordapp.com/api/guilds/774471080713781259/widget.png?style=banner2" />
</a>

---

MIT licensed. © Meta Platforms, Inc. and affiliates; © Callstack; © ReactVision, Inc.
