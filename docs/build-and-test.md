---
title: Build and test
description: How to build and test the widget from the source repository.
---

The source code is on [GitHub](https://github.com/aichatwatch/aicw-summarize). The widget is MIT licensed. To report a bug, open an issue on GitHub.

## Requirements

You need Node.js 18 or newer.

## Set up

Clone the repository.

```sh
git clone https://github.com/aichatwatch/aicw-summarize.git
```

Go into the folder.

```sh
cd aicw-summarize
```

Install the build tool.

```sh
npm install
```

## Source files

- `src/widget.js` is the widget source. Edit this file.
- `dist/aicw-summarize.min.js` is the built file.
- `build.js` checks the source and builds the minified file with `terser`.
- `scripts/safety-check.js` checks the source and the built file for unsafe patterns.

## Commands

This command builds the minified file.

```sh
npm run build
```

This command rebuilds the file each time `src/widget.js` changes.

```sh
npm run dev
```

This command checks the syntax of the source. It does not build.

```sh
npm run validate
```

This command runs the safety check.

```sh
npm run safety
```

This command runs both checks. Run it before you open a pull request.

```sh
npm test
```

## What the safety check does

The safety check reads `src/widget.js` and `dist/aicw-summarize.min.js`. It fails if the widget code does any of these things:

- It changes the root element or the body styles of the host page.
- It sets opacity, filter, or backdrop filter styles.
- It uses a CSS selector that is not scoped under `#aicw-ask-ai-bar` or `#aicw-ask-ai-popup`.

These rules keep the widget from changing the look of the page that hosts it.

## Releases

A GitHub workflow creates a new release when a push to the main branch changes `src/`, `build.js`, `package.json`, or `dist/`. The release tag is the date and time in the format `vYYYYMMDD.HHMMSS`. The workflow runs `npm run validate` first.

For more help, open an issue on [GitHub](https://github.com/aichatwatch/aicw-summarize/issues).
