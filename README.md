# danger-plugin-istanbul-coverage

[![Build Status](https://travis-ci.org/DarcyRayner/danger-plugin-istanbul-coverage.svg?branch=master)](https://travis-ci.org/DarcyRayner/danger-plugin-istanbul-coverage)
[![npm version](https://badge.fury.io/js/danger-plugin-istanbul-coverage.svg)](https://badge.fury.io/js/danger-plugin-istanbul-coverage)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

> Danger.js plugin for monitoring code coverage on changed files.

## Usage

Install:

```sh
yarn add danger-plugin-istanbul-coverage --dev
```

At a glance:

```js
// dangerfile.js
import istanbulCoverage from 'danger-plugin-istanbul-coverage'

istanbulCoverage() // Use default configuration

istanbulCoverage({
  // The location of the istanbul coverage file.
  coveragePath: "./coverage/coverage-summary.json",
  // Which set of files to report from the coverage file.
  reportChangeType: "all", // || "modified" || "created" || "createdOrModified"
  // What to do when the PR doesn't meet the minimum coverage threshold
  reportMode: "message", // || "warn" || "fail"
  threshold: {
    statements: 100,
    branches: 100,
    functions: 100,
    lines: 100,
    },
})
```

This plugin requires the 'json-summary' report mode be enabled with Istanbul.

## Changelog

See the GitHub [release history](https://github.com/DarcyRayner/danger-plugin-istanbul-coverage/releases).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).
