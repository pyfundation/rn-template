# :iphone: React Native Template TypeScript

[![npm downloads](https://img.shields.io/npm/dt/@hmarques98/react-native-template-typescript.svg)](https://www.npmjs.com/package/@hmarques98/react-native-template-typescript)
[![npm version](https://img.shields.io/npm/v/@hmarques98/react-native-template-typescript?color=44BC1C)](https://www.npmjs.com/package/@hmarques98/react-native-template-typescript)
[![Publish and increment to NPM](https://github.com/hmarques98/template-react-native-typescript/actions/workflows/publishNPM.yml/badge.svg)](https://github.com/hmarques98/template-react-native-typescript/actions/workflows/publishNPM.yml)

<p align="center" >
  <img
    height="480px"
    src="docs/assets/list_loaded.png"
    alt="Template landing screen preview"
  />
</p>

<br/>

An opinionated template to bootstrap your next React Native app with all the time-wasting packages you need to have.

In this template is started with example fetching datas from Star Wars Api, where is showing Peoples with Name and HomeWorld and in the next screen when on pressed more details about People. In /docs/assets there are more photos.
## :star: Features in this template 
- React Query for easy and more controlled requisitions.
- CodePush integration.
- Fastlane integration for automated builds.
- BootSplash for faster splashScreen configurations.
- Redux Toolkit for easy global state management.
- StoryBook for components documentation.
- React Testing Library and Detox for automated tests. 
- Sentry for see logs in production.
- And so much more.

## :computer: Contributions are very welcome 🤝

### Let's build the best React Native template together 🚀

Preconfigured with

- Synced with the recommended [TypeScript template](https://reactnative.dev/docs/typescript#getting-started-with-typescript)
- [Storybook](https://github.com/storybookjs/storybook/) The UI component explorer. Develop, document, & test React Native components
- [React Query](https://github.com/tannerlinsley/react-query) for api calls
- [Axios](https://github.com/tannerlinsley/react-query) for fetch api calls
- [Redux Toolkit](https://redux-toolkit.js.org/) for global state.
- [React Navigation](https://reactnavigation.org/) (**v5**) for navigation and deeplinking.
- [styled-components](https://github.com/styled-components/styled-components)
- [styled-system](https://github.com/styled-system/styled-system)
- [react-native-bootsplash](https://github.com/zoontek/react-native-bootsplash) because splash screens are cool.
- [react-native-svg](https://github.com/react-native-community/react-native-svg) because svg.
- [react-native-config](https://github.com/luggit/react-native-config) to manage separate environments (dev, staging, production).
- [Reanimated](https://software-mansion.github.io/react-native-reanimated/) for animations.
- [react-native-keychain](https://github.com/oblador/react-native-keychain) for Keychain/Keystore access.
- [react-native-permissions](https://github.com/zoontek/react-native-permissions) unified permissions api for iOS and Android.
- [NetInfo](https://github.com/react-native-netinfo/react-native-netinfo) Network Info API for Android, iOS, macOS & Windows.
- [react-native-appstate-hook](https://github.com/amrlabib/react-native-appstate-hook) handle app state in your app.
- [react-native-file-logger](https://github.com/BeTomorrow/react-native-file-logger) to log important stuff.
- [react-i18next](https://github.com/i18next/react-i18next) internationalization.
- [AsyncStorage](https://github.com/react-native-community/async-storage) you're gonna install it anyway.
- [FastImage](https://github.com/DylanVann/react-native-fast-image) its more performant
- [Mirage JS](https://miragejs.com/) the easiest way to mock APIs.
- [Fastlane](http://fastlane.tools/) for automation.
- [Code Push](https://github.com/microsoft/react-native-code-push) syncronize JavaScript and Images with over-the-air updates.
- handy npm scripts.
- [react-native-testing-library](https://callstack.github.io/react-native-testing-library/) for unit and component tests.
- [Sentry](https://github.com/getsentry/sentry-react-native) for debugging in production.
- [Detox](https://github.com/wix/Detox) for e2e.

## Contents

- [Documentation](#documentation)
- [Getting Started](#getting-started)
- [Optional Steps](#optional-steps)
- [Credits](#credits)

## Documentation

- [Libraries](#libraries)
- [Directory Structure](#directory-structure)
- [Quick Overview](#quick-overview)
- [File Walkthrough](./docs/file-walkthrough.md)

## Getting Started

Create a new project using the template.

- **Note:** the command will fail if you have the global legacy react-native-cli installed. Make sure you uninstall it first. More info at [react-native-community/cli](https://github.com/react-native-community/cli#about).

### RN 0.64.1

```bash
$ npx react-native init MyApp --template @hmarques98/react-native-template-typescript
```

## Road Map

- Finish Detox integration
- Add Docusaurs docs
- [Codepush Code Signing](https://github.com/microsoft/code-push/tree/v3.0.1/cli#code-signing)

## Optional Steps

#### Connect To Sentry

This template comes with [Sentry](https://github.com/getsentry/sentry-react-native), but its disabled until you connect your account.

To connect your account:

```bash
$ cd MyApp/

# For MacOS
$ npx sentry-wizard -i reactNative -p ios android

# Other Platforms
$ npx sentry-wizard -i reactNative -p android
```

Insert your sentry DSN in each [.env](https://github.com/osamaq/react-native-template/blob/ed37c213eacf0681c4f50f959bad170d46be0ed7/template/.env.prod#L5) file (dev, staging and production) and you're all done.

### Setup deep linking scheme

Implementation was based on react-navigation[instructions](https://reactnavigation.org/docs/deep-linking/#set-up-with-bare-react-native-projects).

1. Update the prefix with wanted URI in `App.tsx`

1. iOS

Update `CFBundleURLName` and `CFBundleURLSchemes` to your desired URI

1. Android

Update `android:scheme` value inside `<data>` tag from the `<intent-filter>`

#### Enable Push Notification capability from Xcode

You must be a member of the Apple Developer Program in order to enable Push Notifications

![Instructions to add push notifications capability](https://i.stack.imgur.com/qsQTx.jpg)

### Setup OneSignal

1. You will need to have [OneSignal Account](https://app.onesignal.com/signup)
2. Your OneSignal App ID, available in [Keys & IDs
   iOS.](https://documentation.onesignal.com/docs/accounts-and-keys#section-app-id)

3. IOS - [Generate an iOS Push Certificate.](https://documentation.onesignal.com/docs/generate-an-ios-push-certificate) You should generate a certificate after adding the Push Notification capability while setting up your iOS app.
4. Android - [Generate a Google Firebase Server API Key](https://documentation.onesignal.com/docs/generate-a-google-server-api-key)
5. Optional step for your application to use [Confirmed Deliveries](https://documentation.onesignal.com/docs/confirmed-deliveries) and and increment/decrement [Badges](https://documentation.onesignal.com/docs/badges) through push notifications, you need to set up an App Group for your application.

In your main app target go back to Signing & Capabilities > All > + Capability and add App Groups

![Instructions to add push notifications capability](https://files.readme.io/5b72690-Screen_Shot_2020-08-15_at_6.10.59_PM.png)

![Instructions to add push notifications capability](https://files.readme.io/2f271ce-Screen_Shot_2020-08-15_at_6.15.25_PM.png)

![Instructions to add push notifications capability](https://files.readme.io/230100f-c51bffb-Screen_Shot_2020-08-15_at_6.21.25_PM.png)

For more instructions and doubts, go to [Documentation Integration](https://documentation.onesignal.com/docs/react-native-sdk-setup#step-4-install-for-ios-using-cocoapods-for-ios-apps)

### Setup Code Push

1. You will need to have [AppCenter CLI](https://github.com/microsoft/appcenter-cli) installed

1. Creating an AppCenter account and/or organization and create an app for each platform and environment

1. Copy and Replace the CodePushDeploymentKey in android/app/build.gradle under `buildTypes`

1. Copy and Replace the CodePushDeploymentKey in android/app/build.gradle and XCode -> YourProject -> Build Settings -> `CODE_PUSH_KEY`

You can retrieve this values by running `appcenter codepush deployment list -a <ownerName>/<appName> -k`

## Libraries

Let's briefly go over the benefit of each library included in this template.

### TypeScript

For type safety ¯\\_(ツ)_/¯

But in all seriousness, if you are considering this template I assume you are a TypeScript fan. If you happen to be a JavaScript user, this template might be overwhelming. If you would like to start learning TypeScript, I suggest bootstrapping with this instead [react-native-community/react-native-template-typescript](https://github.com/react-native-community/react-native-template-typescript) so you can learn at your own pace.

### styled-components

Style your apps without stress with dynamic styling and painless maintenance. `styled-components` utilises tagged template literals to style your component. Checkout this [Getting started tutorial](https://styled-components.com/docs/basics#getting-started).

### styled-system

Styled System is a collection of utility functions that add style props to your React components and allows you to control styles based on a global theme object with typographic scales, colors, and layout properties. Checkout this [Getting started tutorial](https://styled-system.com/#getting-started).

### React Query

Hooks for fetching, caching and updating asynchronous data in React.

- Alternative: SWR/Apollo.

### AXIOS

I like to used axios because your interceptors configurations.

### Redux/Redux Toolkit

I'm happy using Redux Toolkit. It's a lot more concise now and I enjoy the redux ecosystem of plugins.

SWR reduces our dependency on Redux for global state. And sometimes React Navigation can be used to send data to the next screen. I try to leverage these two before reaching out to global state.

If you prefer something else, remove redux and go with that. Do not waste time trying a new state management solution.

### React Navigation

It is the most popular navigation library. For most apps, this is the best choice.

### react-native-keychain

Save and use credentials from phone's Keychain/Keystore

### react-native-permissions

A unified permissions API for React Native on iOS and Android. For iOS you have to the `Podfile` with permissions pod and update `Info.plist` with wanted permissions descriptions. For Android add wanted permissions in `AndroidManifest.xml`

### react-i18next

Localization using hooks. [React Native example](https://github.com/i18next/react-i18next/tree/master/example/react-native)

### OneSignal

OneSignal is the fastest and most reliable service to send push notifications, in-app messages, and emails to your users on mobile

### Codepush

A React Native app is composed of JavaScript files and any accompanying images, which are bundled together by the packager and distributed as part of a platform-specific binary (i.e. an .ipa or .apk file). Once the app is released, updating either the JavaScript code (e.g. making bug fixes, adding new features) or image assets, requires you to recompile and redistribute the entire binary, which of course, includes any review time associated with the store(s) you are publishing to.

The CodePush plugin helps get product improvements in front of your end users instantly, by keeping your JavaScript and images synchronized with updates you release to the CodePush server. This way, your app gets the benefits of an offline mobile experience, as well as the "web-like" agility of side-loading updates as soon as they are available. It's a win-win!

### Sentry

Benefitial in debugging issues that occur only in release builds. You can view error stack traces for unhandled exceptions. You can also choose to log specific errors in some catch blocks to study how often they occur in production.

### react-native-bootsplash

Works great for controlling your splash screen.
To help about lib

```bash
$ npx react-native generate-bootsplash --help
```

Full command usage example to put your SplashScreen

```bash
npx react-native generate-bootsplash assets/splash.png \
  --background-color=F5FCFF \
  --logo-width=100 \
  --assets-path=assets \
  --flavor=main
```

Only iOS follow this instructions from library [BootSplash](https://github.com/zoontek/react-native-bootsplash)
where is saying `Set the BootSplash.storyboard as launch screen file:`

### react-native-svg

Prefer using SVG over images all the time (remember to optimize your SVGs).

### react-native-config

If you have different development, staging and production variables, this library is very helpful. It allows you to declare environment variables that can be accessed by all 3 sides (android, ios, JavaScript).

Android: by default, running `react-native run-android` will use the development .env file. To load .env.staging we must use:

`ENVFILE=.env.staging react-native run-android`

> Note: the above works on MacOS. For windows its a bit different. See [Different Environments](https://github.com/luggit/react-native-config#different-environments).

iOS: two additional schemes are created in the Xcode project for staging and production. The corresponding .env file is set via the scheme's pre-action:

<div align="center">
    <img src="docs/assets/scheme.png" alt="Scheme's pre-action setting the .env file" width="100%">
</div>

NPM scripts for running the app with the desired configuration are [included](https://github.com/osamaq/react-native-template/blob/acc4f4ab117bee099a531ad44be1130f9d24df69/template/package.json#L11) for convenience.

### Reanimated

Necessary when creating complex gesture based animations that are highly performant.

### Lottie React Native

Lottie is a mobile library for Android and iOS that parses Adobe After Effects animations exported as JSON with bodymovin and renders them natively on mobile!

For the first time, designers can create and ship beautiful animations without an engineer painstakingly recreating it by hand.

### react-native-appstate-hook

Custom react hook, built to handle iOS or Android appState in your react component.

### react-native-file-logger

A simple file-logger for React Native with configurable rolling policy, based on CocoaLumberjack on iOS and Logback on Android.

### AsyncStorage

For caching simple data such as user perferences.

### FastImage

Drop in replacement for the `<Image/>` component. I've found this to give a performance boost on android when rendering many images.

### NetInfo

Network Info API for Android, iOS, macOS & Windows. It allows you to get information on:

- Connection type
- Connection quality

### react-native-testing-library

For unit and component testing.

### Detox

For end-to-end testing.

### Mirage JS

Mirage is an in-memory server for intercepting API calls and returning whatever data you want. Very useful for developing before the backend is deployed, and for confirming how the app reacts to different API call outcomes.

### Fastlane

Fastlane community has an endless amount of mobile development automation plugins. I currently use it mainly for [automatic versioning](https://osamaq.com/automatic-versioning-for-react-native-apps/), and often for deploying to Microsoft's App Center in [one command](https://github.com/osamaq/reactnative-fastlane-appcenter).

This template also has a [fastlane command](https://github.com/osamaq/react-native-template/blob/acc4f4ab117bee099a531ad44be1130f9d24df69/template/fastlane/Fastfile#L203) for adding version badges to app icons. Useful outside of production as it makes it easier for QA to tell the app version.

<div align="center">
    <img src="docs/assets/ic_launcher.png" alt="App icon with version badge" width="20%">
</div>

---

> _If you appreciate those libraries and find them useful, please consider supporting them._

## Directory Structure

```
root
├── __mocks__
├── __tests__
├── android
├── ios
├── storybook
|   └── addons.js
|   └── index.js
|   └── rn_addons.js
└── src
    └── components
    |   └── molecules
            └── Box
              └── Box.tsx
              └── index.tsx
              └── stories.tsx 
            └── Button
              └── Button.tsx
              └── index.tsx
              └── stories.tsx 
            └── Typography
              └── Typography.tsx
              └── index.tsx
              └── stories.tsx 
    |   └── organisms
            └── CardPeoples.tsx
    |   └── StatusBar.tsx
    |   └── stories.ts
    └── hooks
    |   └── useCustomBackBehaviour.tsx
    |   └── useInfinityQuery.tsx
    |   └── useReactQuery.tsx
    |   └── useOneSignal.tsx
    |   └── useStartupTime.tsx
    └── interfaces
    |   └── IPeople.ts
    └── localization
    |   └── resources
    |   |   └── en.json
    |   |   └── index.ts
    |   |   └── ro.json
    |   └── index.tsx
    └── navigation
    |   └── RootNavigation.tsx
    |   └── Router.tsx
    └── navigation
    |   ├── RootNavigation.tsx
    |   └── Router.tsx
    └── screens
    |   ├── CharacterDetail.tsx
    |   ├── Home.tsx
    |   ├── index.ts
    └── utils
        ├── constants.ts
        └── console.ts
    └── services
        ├── axios.ts
    └── store
        └── slices
          └── auth.ts
          └── index.ts
        └── index.ts
        └── rootReducer.ts
    └── styles
        ├── colors.ts
        ├── typography.ts
        ├── spacing.ts
        ├── index.ts
├── plop-templates
  └── CommonScreen.js.hbs
  └── Component.js.hbs
  └── ExportIndex.js.hbs
  └── Stories.js.hbs
├── e2e
├── assets
├── fastlane
```

## Credits

This template is modified from [react-native-typescript-template](https://github.com/react-native-community/react-native-template-typescript) and inspired from Osama Qarem's [React Native template](https://github.com/osamaqarem/react-native-template) and also inspired from Gabriel Moncea [React Native template](https://github.com/gabrielmoncea/react-native-template)

Thank you ❤️
