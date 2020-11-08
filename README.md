# Messaging Kata - TypeScript

## Deliverable
A simple messaging application, built in Node.js using TypeScript. This application must be able to send and store simple textual messages that can then be retrieved via a RESTful API. This project should take between 2 - 4 hours.

## MVP Requirements

- This application must be presented via a private GitHub repository. When you're done, please add me as a contributor to your private Github repository.
- This application must be unit tested. Please use Jest.
- The data that is stored must be accessible via a RESTful API. You can store in memory or a DB
- A README file with documentation on: how to build it, how to use it, how to run the tests

### Create thread
Creates a thread on behalf of a user.

#### Request
```
POST /thread 
{
    "users": [
        "jeff_goldblum",
    ]
}
```

#### Response
```
{
    "thread_id": 123
}
```

### Send message
Creates a message on behalf of a user on a thread.

#### Request
```
POST /thread/:thread_id/:username
{
    "message": "This is a message!"
}
```

#### Response
```
204
```

### Get thread
Returns a list of messages by thread ID

#### Request
```
GET /thread/:thread_id
```

#### Response
```
{
    "messages": [
        {"username": "jeff_goldblum", "message": "This is a message!"},
        ...
    ]
}
```

### Bonus
- Include a database for storage instead of in memory
- Include a functioning React user interface on top of the RESTful API (even more bonus for tests!)
- Make it function in real-time using sockets

# Template Description

[![TypeScript version][ts-badge]][typescript-38]
[![Node.js version][nodejs-badge]][nodejs]
[![APLv2][license-badge]][LICENSE]
[![Build Status - Travis][travis-badge]][travis-ci]
[![Build Status - GitHub Actions][gha-badge]][gha-ci]
[![Sponsor][sponsor-badge]][sponsor]

# node-typescript-boilerplate

👩🏻‍💻 Developer Ready: A comprehensive template. Works out of the box for most [Node.js][nodejs] projects.

🏃🏽 Instant Value: All basic tools included and configured:

+ [TypeScript][typescript] [3.8][typescript-38]
+ [ESLint][eslint] with some initial rules recommendation
+ [Jest][jest] for fast unit testing and code coverage
+ Type definitions for Node.js and Jest
+ [Prettier][prettier] to enforce consistent code style
+ NPM [scripts](#available-scripts) for common operations
+ simple example of TypeScript code and unit test
+ .editorconfig for consistent file format
+ example configuration for [GitHub Actions][gh-actions] and [Travis CI][travis]

🤲 Free as in speach: available under the APLv2 license.

## Getting Started

This project is intended to be used with the latest Active LTS release of [Node.js][nodejs].

### Use as a repository template

To start, just click the **[Use template][repo-template-action]** link (or the green button). Now start adding your code in the `src` and unit tests in the `__tests__` directories.

### Clone repository

To clone the repository use the following commands:

```sh
git clone https://github.com/jsynowiec/node-typescript-boilerplate
cd node-typescript-boilerplate
npm install
```

### Download latest release

Download and unzip current `master` branch or one of tags:

```sh
wget https://github.com/jsynowiec/node-typescript-boilerplate/archive/master.zip -O node-typescript-boilerplate.zip
unzip node-typescript-boilerplate.zip && rm node-typescript-boilerplate.zip
```

## Available Scripts

+ `clean` - remove coverage data, Jest cache and transpiled files,
+ `build` - transpile TypeScript to ES6,
+ `build:watch` - interactive watch mode to automatically transpile source files,
+ `lint` - lint source files and tests,
+ `test` - run tests,
+ `test:watch` - interactive watch mode to automatically re-run tests

## Additional Informations

### Writing tests in JavaScript

Writing unit tests in TypeScript can sometimes be troublesome and confusing. Especially when mocking dependencies and using spies.

This is **optional**, but if you want to learn how to write JavaScript tests for TypeScript modules, read the [corresponding wiki page][wiki-js-tests].

## Backers & Sponsors

Support this project by becoming a sponsor.

## License
Licensed under the APLv2. See the [LICENSE](https://github.com/jsynowiec/node-typescript-boilerplate/blob/master/LICENSE) file for details.

[ts-badge]: https://img.shields.io/badge/TypeScript-3.8-blue.svg
[nodejs-badge]: https://img.shields.io/badge/Node.js->=%2012.13-blue.svg
[nodejs]: https://nodejs.org/dist/latest-v12.x/docs/api/
[travis-badge]: https://travis-ci.org/jsynowiec/node-typescript-boilerplate.svg?branch=master
[travis-ci]: https://travis-ci.org/jsynowiec/node-typescript-boilerplate
[gha-badge]: https://img.shields.io/endpoint.svg?url=https%3A%2F%2Factions-badge.atrox.dev%2Fjsynowiec%2Fnode-typescript-boilerplate%2Fbadge&style=flat
[gha-ci]: https://github.com/jsynowiec/node-typescript-boilerplate/actions
[typescript]: https://www.typescriptlang.org/
[typescript-38]: https://www.typescriptlang.org/docs/handbook/release-notes/typescript-3-8.html
[license-badge]: https://img.shields.io/badge/license-APLv2-blue.svg
[license]: https://github.com/jsynowiec/node-typescript-boilerplate/blob/master/LICENSE

[sponsor-badge]: https://img.shields.io/badge/♥-Sponsor-fc0fb5.svg
[sponsor]: https://github.com/sponsors/jsynowiec

[jest]: https://facebook.github.io/jest/
[eslint]: https://github.com/eslint/eslint
[wiki-js-tests]: https://github.com/jsynowiec/node-typescript-boilerplate/wiki/Unit-tests-in-plain-JavaScript
[prettier]: https://prettier.io
[gh-actions]: https://github.com/features/actions
[travis]: https://travis-ci.org

[repo-template-action]: https://github.com/jsynowiec/node-typescript-boilerplate/generate
