# Tik Tok UI Clone
TikTok, also known as Douyin in China, is a media app for creating and sharing short videos.

## What is the purpose of this repository?

I created this repository to study React Native and try to recreate several famous app designs.

## Prerequisites

- Git (https://git-scm.com/)
- Node (https://nodejs.org)
- Android Studio (https://developer.android.com/studio)
- Emulator or ADB device

## Software Requirements(At least)
  - Node: 12.9.1
  - Yarn: 1.21.1
  - npm: 6.13.7

## How to install?

The first thing we have to do is download the repository for our development environment

```sh
git clone https://github.com/ReinanHS/tiktok-ui.git
npm install -g yarn
```

Run the following command to download the project's dependencies

```sh
yarn install
```
To run the app in development mode :
```sh
yarn android
   or
yarn ios
```


### If your NodeJS version is greater than 12.10

```txt
Expo fails to start the project: error Invalid regular expression: /(.*\\__fixtures__
```

If you have a problem with this error, follow these steps

to solve this problem you have to change this file `\node_modules\metro-config\src\defaults\blacklist.js` there is an invalid regular expression that needed changed. I changed the first expression under `sharedBlacklist` from:

```js
var sharedBlacklist = [
  /node_modules[/\\]react[/\\]dist[/\\].*/,
  /website\/node_modules\/.*/,
  /heapCapture\/bundle\.js/,
  /.*\/__tests__\/.*/
];
```

to:

```js
var sharedBlacklist = [
  /node_modules[\/\\]react[\/\\]dist[\/\\].*/,
  /website\/node_modules\/.*/,
  /heapCapture\/bundle\.js/,
  /.*\/__tests__\/.*/
];
```