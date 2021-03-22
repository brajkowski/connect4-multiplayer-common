# Connect 4 Multiplayer: Common

[![Build](https://github.com/brajkowski/connect4-multiplayer-common/actions/workflows/build.yml/badge.svg)](https://github.com/brajkowski/connect4-multiplayer-common/actions/workflows/build.yml)
[![npm:latest](https://img.shields.io/npm/v/@brajkowski/connect4-multiplayer-common/latest?color=limegreen&logo=npm)](https://www.npmjs.com/package/@brajkowski/connect4-multiplayer-common)
[![npm:beta](https://img.shields.io/npm/v/@brajkowski/connect4-multiplayer-common/beta?logo=npm)](https://www.npmjs.com/package/@brajkowski/connect4-multiplayer-common)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

This library provides shared objects used by both the connect 4 multiplayer client and server.

## Installation

Using npm:

```
$ npm i --save @brajkowski/connect4-multiplayer-common
```

## Usage

### Common Interfaces

This library provides the following interfaces:

```ts
let ca: ClientAction;
let cp: ClientPacket;
let sa: ServerAction;
let sp: ServerPacket;
```

## Building from Source

Using npm:

```
$ npm run build
```

will produce the compiled library under `/dist`.
