@talkyjs/cli
============

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/@talkyjs/cli.svg)](https://npmjs.org/package/@talkyjs/cli)
[![Downloads/week](https://img.shields.io/npm/dw/@talkyjs/cli.svg)](https://npmjs.org/package/@talkyjs/cli)
[![License](https://img.shields.io/npm/l/@talkyjs/cli.svg)](https://github.com/ask-utils/talkyjs-cli/ask-utils/talkyjs-cli/blob/master/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g @talkyjs/cli
$ talky COMMAND
running command...
$ talky (-v|--version|version)
@talkyjs/cli/0.0.0 darwin-x64 node-v12.9.1
$ talky --help [COMMAND]
USAGE
  $ talky COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`talky new [FILE]`](#talky-new-file)
* [`talky generate TYPE`](#talky-generate-type)
* [`talky help [COMMAND]`](#talky-help-command)

## `talky new [FILE]`

Create a new Alexa app

```
USAGE
  $ talky new

OPTIONS
  -B, --database=(none|s3|dynamodb)  [default: none] Skill database type
  -D, --dry-run
  -P, --path=path                    [default: ./] target path
  -S, --ssml=(tsx|default)           [default: tsx] SSML markup type
  -T, --no-test                      Ignore default test code
  -d, --debug
  -h, --help                         show CLI help
```

### Created files by default

```bash
% tree -I node_modules 
.
├── README.md
├── package-lock.json
├── package.json
├── src
│   ├── HelpIntent
│   │   ├── HelpIntent.router.ts
│   │   ├── HelpIntent.speech.tsx
│   │   └── tests
│   │       ├── HelpIntent.router.spec.ts
│   │       └── HelpIntent.speech.spec.tsx
│   ├── LaunchRequest
│   │   ├── LaunchRequest.router.ts
│   │   ├── LaunchRequest.speech.tsx
│   │   └── tests
│   │       ├── LaunchRequest.router.spec.ts
│   │       └── LaunchRequest.speech.spec.tsx
│   ├── StopAndCancelAndNoIntent
│   │   ├── StopAndCancelAndNoIntent.router.ts
│   │   ├── StopAndCancelAndNoIntent.speech.tsx
│   │   └── tests
│   │       ├── StopAndCancelAndNoIntent.router.spec.ts
│   │       └── StopAndCancelAndNoIntent.speech.spec.tsx
│   ├── index.ts
│   └── tests
│       └── index.spec.ts
├── tsconfig.json
└── webpack.config.ts

8 directories, 19 files
```

_See code: [src/commands/new.ts](https://github.com/ask-utils/talkyjs-cli/blob/v0.0.0/src/commands/new.ts)_

## `talky generate TYPE`

[g, gen, generate] Generate files

```
USAGE
  $ talky generate TYPE NAME

ARGUMENTS
  TYPE  (handler|router|service) Generate file type
  NAME  Generate files name

OPTIONS
  -D, --dry-run
  -P, --path=path           [default: ./src] generate file path
  -S, --ssml=(tsx|default)  SSML markup type
  -T, --no-test             Ignore default test code
  -d, --debug
  -h, --help                show CLI help

ALIASES
  $ talky g
  $ talky gen
```

_See code: [src/commands/generate.ts](https://github.com/ask-utils/talkyjs-cli/blob/v0.0.0/src/commands/generate.ts)_

## `talky help [COMMAND]`

display help for talky

```
USAGE
  $ talky help [COMMAND]

ARGUMENTS
  COMMAND  command to show help for

OPTIONS
  --all  see all commands in CLI
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v3.1.0/src/commands/help.ts)_

<!-- commandsstop -->
