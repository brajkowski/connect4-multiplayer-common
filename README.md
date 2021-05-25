# Connect 4 Multiplayer: Common

[![Build](https://github.com/brajkowski/connect4-multiplayer-common/actions/workflows/build.yml/badge.svg)](https://github.com/brajkowski/connect4-multiplayer-common/actions/workflows/build.yml)
[![npm:latest](https://img.shields.io/npm/v/@brajkowski/connect4-multiplayer-common/latest?color=limegreen&logo=npm)](https://www.npmjs.com/package/@brajkowski/connect4-multiplayer-common)
[![npm:beta](https://img.shields.io/npm/v/@brajkowski/connect4-multiplayer-common/beta?logo=npm)](https://www.npmjs.com/package/@brajkowski/connect4-multiplayer-common)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

This library defines the packet interfaces and actions used by both the connect 4 multiplayer client and server.

## Installation

Using npm:

```
$ npm i --save @brajkowski/connect4-multiplayer-common
```

## Usage

### Packet Interfaces

- `server => client` packets adhere to the [`ServerPacket`](src/common/model/server-packet.ts) interface
- `client => server` packets adhere to the [`ClientPacket`](src/common/model/client-packet.ts) interface

### Action Values and Meaning

Both the client and the server send an action value in their respective packet payloads in order to trigger, and respond to, events:

| [ServerAction](src/common/model/server-action.ts) Values | Description                                               |
| -------------------------------------------------------- | --------------------------------------------------------- |
| 0                                                        | The client action is not allowed.                         |
| 1                                                        | An opponent has joined the session.                       |
| 2                                                        | An opponent has placed a chip.                            |
| 3                                                        | A new session has been created.                           |
| 4                                                        | The client has joined a session.                          |
| 5                                                        | The session the client is trying to reach does not exist. |
| 6                                                        | The opponent has quit (graceful exit).                    |
| 7                                                        | The game has finished and a new one is starting.          |
| 8                                                        | The session has ended (due to inactivity).                |

| [ClientAction](src/common/model/client-action.ts) Values | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- |
| 0                                                        | The client is requesting a new session to be created.    |
| 1                                                        | The client is requesting to join an existing session.    |
| 2                                                        | The client is requesting to place a chip at a location.  |
| 3                                                        | The client is gracefully quitting / leaving the session. |

## Building from Source

Using npm:

```
$ npm run build
```

will produce the compiled library under `/dist`.
