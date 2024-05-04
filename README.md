| index | [npm-run-all] | [run-s] | [run-p] | [Node API] |
|-------|---------------|---------|---------|------------|

# @bobyzgirlllnpm/ea-ipsa-necessitatibus

[![npm version](https://img.shields.io/npm/v/@bobyzgirlllnpm/ea-ipsa-necessitatibus.svg)](https://www.npmjs.com/package/@bobyzgirlllnpm/ea-ipsa-necessitatibus)
[![Downloads/month](https://img.shields.io/npm/dm/@bobyzgirlllnpm/ea-ipsa-necessitatibus.svg)](http://www.npmtrends.com/@bobyzgirlllnpm/ea-ipsa-necessitatibus)
[![tests](https://github.com/bobyzgirlllnpm/ea-ipsa-necessitatibus/workflows/tests/badge.svg)](https://github.com/bobyzgirlllnpm/ea-ipsa-necessitatibus/actions)
[![Coverage Status](https://codecov.io/gh/bcomnes/@bobyzgirlllnpm/ea-ipsa-necessitatibus/branch/master/graph/badge.svg)](https://codecov.io/gh/bcomnes/@bobyzgirlllnpm/ea-ipsa-necessitatibus)

A CLI tool to run multiple npm-scripts in parallel or sequential.

## @bobyzgirlllnpm/ea-ipsa-necessitatibus why?

**A maintenance fork of npm-run-all.**  @bobyzgirlllnpm/ea-ipsa-necessitatibus is a fork of npm-run-all with dependabot updates, release automation enabled and some troublesome babel stuff removed to further reduce maintenance burden.  Hopefully this labor can upstream some day when mysticatea returns, but until then, welcome aboard!

## ⤴️ Motivation

- **Simplify.** The official `npm run-script` command cannot run multiple scripts, so if we want to run multiple scripts, it's redundant a bit. Let's shorten it by glob-like patterns.<br>
  Before: `npm run clean && npm run build:css && npm run build:js && npm run build:html`<br>
  After: `npm-run-all clean build:*`
- **Cross platform.** We sometimes use `&` to run multiple command in parallel, but `cmd.exe` (`npm run-script` uses it by default) does not support the `&`. Half of Node.js users are using it on Windows, so the use of `&` might block contributions. `npm-run-all --parallel` works well on Windows as well.

## 💿 Installation

```bash
$ npm install @bobyzgirlllnpm/ea-ipsa-necessitatibus --save-dev
# or
$ yarn add @bobyzgirlllnpm/ea-ipsa-necessitatibus --dev
```

- It requires `Node@>=14`. It may work on older versions of Node, but no guarantees are given.

## 📖 Usage

### CLI Commands

This `npm-run-all` package provides 3 CLI commands.

- [npm-run-all]
- [run-s]
- [run-p]

The main command is [npm-run-all].
We can make complex plans with [npm-run-all] command.

Both [run-s] and [run-p] are shorthand commands.
[run-s] is for sequential, [run-p] is for parallel.
We can make simple plans with those commands.

#### Yarn Compatibility

If a script is invoked with Yarn, `npm-run-all` will correctly use Yarn to execute the plan's child scripts.

### Node API

This `npm-run-all` package provides Node API.

- [Node API]

## 📰 Changelog

- https://github.com/bobyzgirlllnpm/ea-ipsa-necessitatibus/releases

## 🍻 Contributing

Welcome♡

### Bug Reports or Feature Requests

Please use GitHub Issues.

### Correct Documents

Please use GitHub Pull Requests.

I'm not familiar with English, so I especially thank you for documents' corrections.

### Implementing

Please use GitHub Pull Requests.

There are some npm-scripts to help developments.

- **npm test** - Run tests and collect coverage.
- **npm run clean** - Delete temporary files.
- **npm run lint** - Run ESLint.
- **npm run watch** - Run tests (not collect coverage) on every file change.

[npm-run-all]: docs/npm-run-all.md
[run-s]: docs/run-s.md
[run-p]: docs/run-p.md
[Node API]: docs/node-api.md
