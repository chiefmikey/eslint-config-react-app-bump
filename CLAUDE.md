# Project CLAUDE.md - eslint-config-react-app-bump

## Project Overview

A fork of `eslint-config-react-app` (from Create React App) with updated dependencies. Published as `eslint-config-react-app-bump` on npm. Provides ESLint rules for React projects including TypeScript, JSX accessibility, React Hooks, Flow, and Jest support.

## Tech Stack

- **Language:** JavaScript (CommonJS)
- **ESLint:** v8 (legacy config format, not flat config)
- **Node:** >= 14.0.0
- **Dependencies:** @typescript-eslint, eslint-plugin-react, eslint-plugin-react-hooks, eslint-plugin-jsx-a11y, eslint-plugin-import, eslint-plugin-flowtype, eslint-plugin-jest, eslint-plugin-testing-library

## Architecture

```
index.js        # Main config — extends base.js, adds React/JSX/a11y/hooks rules
base.js         # Base ESLint config (parser setup, core rules)
jest.js         # Jest-specific rules (testing-library + jest plugins)
package.json    # Published package config
```

## Commands

No scripts defined. This is a shareable ESLint config — consumed via `extends` in downstream projects.

## Conventions

- CommonJS (`require`/`module.exports`) — not ESM
- Uses `@rushstack/eslint-patch` for dependency resolution
- Peer dependency on `eslint ^8.0.0`
- Version: 1.0.25
- Conventional commits
