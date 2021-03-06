# react-native-template <img src="docs/assets/icon.png" alt="Logo" width="4%">

[![Build Status](https://travis-ci.com/osamaq/react-native-template.svg?branch=master)](https://travis-ci.com/osamaq/react-native-template)
[![npm downloads](https://img.shields.io/npm/dt/@osamaq/react-native-template.svg)](https://www.npmjs.com/package/@osamaq/react-native-template)
[![npm version](https://img.shields.io/npm/v/@osamaq/react-native-template?color=44BC1C)](https://www.npmjs.com/package/@osamaq/react-native-template)

<div align="center">
    <img src="docs/assets/tools.png" alt="Preview" width="100%">
</div>
<br/>

A minimal template with good architecture and common packages to let you focus on writing features right away.

## Preconfigured with

- TypeScript
- [Redux](https://redux.js.org/) with [Redux Toolkit](https://redux-toolkit.js.org/)
- [Redux Observable](https://redux-observable.js.org/)
- [React Navigation](https://reactnavigation.org/) (**v5**)
- [Reactotron](https://github.com/infinitered/reactotron) (and [Flipper](https://fbflipper.com/))
- [Sentry](https://docs.sentry.io/platforms/react-native/) with redux action logging middleware
- [react-native-splash-screen](https://github.com/crazycodeboy/react-native-splash-screen)
- [react-native-svg](https://github.com/react-native-community/react-native-svg)
- [react-native-config](https://github.com/luggit/react-native-config)
- [Reanimated](https://software-mansion.github.io/react-native-reanimated/)
- [Redash](https://wcandillon.github.io/react-native-redash/)
- [AsyncStorage](https://github.com/react-native-community/async-storage)
- [NetInfo](https://github.com/react-native-community/react-native-netinfo)
- [FastImage](https://github.com/DylanVann/react-native-fast-image)
- [<s>Detox</s>](https://github.com/wix/Detox) (WIP – when it supports RN 0.62.x)
- [Fastlane](http://fastlane.tools/)
- [Mirage JS](https://github.com/miragejs/miragejs)
- Other — [error boundary](https://reactjs.org/docs/error-boundaries.html), architecture, services & utils.
- npm/fastlane automation scripts.

## Getting Started

Create a new project using the template.

- **Note:** the command will fail if you have the global legacy react-native-cli installed. Make sure you uninstall it first. More info at [react-native-community/cli](https://github.com/react-native-community/cli#about).

### RN 0.62.2

```bash
$ npx react-native init MyApp --template @osamaq/react-native-template
```

## Optional Steps

#### Connect To Sentry

This template comes with Sentry, but its disabled until you connect your account. It also comes with a [custom middleware](https://github.com/osamaq/react-native-template/blob/master/template/src/redux/middleware/sentryMiddleware.ts) for Redux. What the middleware does is add your redux action types as breadcrumbs to Sentry's crash logs for easier debugging. It does not log payloads, which you might wish do if your app's networking activity is lightweight.

<div align="center">
    <img src="docs/assets/breadcrumbs.png" alt="Logo" width="100%">
</div>

To connect your account:

```bash
$ cd MyApp/

# For MacOS
$ npx sentry-wizard -i reactNative -p ios android

# Other Platforms
$ npx sentry-wizard -i reactNative -p android
```

Insert your DSN in [App.tsx](https://github.com/osamaq/react-native-template/blob/0c1d30722b8364013f712b18fd6abc6fed30edfa/template/App.tsx#L23) and you're all done.

## TODO

- [ ] Add CodePush/OTA
- [ ] i18n
- [ ] Unit Testing Examples
