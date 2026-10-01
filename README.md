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
  <a href="https://discord.gg/A6TaFNqwVc">
    <img src="https://img.shields.io/discord/774471080713781259?label=Discord" alt="Discord">
  </a>
</p>

# visionOS Project Template, By ReactVision

The React Native community template with a `visionos/` folder added, so a new project targets
iOS, Android and Apple Vision Pro from the same JavaScript.

> **Supported with Expo, for now.** ReactVision's visionOS support is announced for Expo apps: the
> config plugin, the setup guide and this template are all verified in that shape. A bare React
> Native app is not supported yet — nothing here is known to break there, but nothing has been
> verified there either.

```bash
npx @react-native-community/cli@latest init MyApp \
  --template @reactvision/visionos-template
```

> The GitHub form `--template github:ReactVision/visionos-template` installs the same thing, and is
> the way to get a commit that has not been published yet.

That gives you `android/`, `ios/` and `visionos/`, with
[`@reactvision/react-native-visionos`](https://github.com/ReactVision/react-native-visionos)
already in `package.json`.

```bash
cd MyApp/visionos
bundle install              # once per project
bundle exec pod install
cd ..
npx react-native run-visionos
```

For an Expo app, follow ViroReact's visionOS setup guide instead: it uses only this template's
`visionos/` folder and lets the config plugin wire it up.

## Adding it to a project you already have

The template only matters when creating a project. To add `visionos/` to an existing app, generate
one into a scratch directory and copy the folder across:

```bash
npx @react-native-community/cli@latest init MyApp \
  --template @reactvision/visionos-template \
  --directory visionos-scratch --skip-install
mv visionos-scratch/visionos ./visionos && rm -rf visionos-scratch
```

Use your app's own name for `MyApp`: the generated Xcode project and app folder are named after it.

## Versions

The template version tracks the React Native line, and the `visionos/` folder is built for that
same line. Its version number follows `@reactvision/react-native-visionos`, so the `react-native`
it pins may be an earlier patch of the same line (template 0.86.4 pins `react-native` 0.86.2). Mixing them is the thing to avoid: a `visionos/` folder from one React Native version
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
