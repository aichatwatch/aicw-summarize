---
title: Installation
description: Add the widget from the jsDelivr CDN, pin a release, or host the file yourself.
---

You can load the widget in three ways. Choose the way that fits your site.

## Use the CDN

The project uses jsDelivr to serve the file. Add this tag right before `</body>`.

```html
<script src=""></script>
```

The `@latest` part points to the newest GitHub release. A new release is created each time a change to `src/`, `build.js`, `package.json`, or `dist/` is pushed to the main branch. Your site then gets the new version without a change from you.

## Pin a release

A pinned release never changes. Use it for production sites. Replace `@latest` with a release tag.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@v20261031.113456/dist/aicw-summarize.min.js"></script>
```

Release tags are dates and times in the format `vYYYYMMDD.HHMMSS`. To see all tags, open the [releases page on GitHub](https://github.com/aichatwatch/aicw-summarize/releases). The tag in the example was the newest one when this page was written.

## Host the file yourself

If you do not want to use a CDN, build the file and copy it to your own server. You need Node.js 18 or newer.

<Steps>
  <Step title="Clone the repository">
    ```sh
    git clone https://github.com/aichatwatch/aicw-summarize.git
    ```
  </Step>
  <Step title="Go into the folder">
    ```sh
    cd aicw-summarize
    ```
  </Step>
  <Step title="Install the build tool">
    The build uses the `terser` minifier. This command installs it.

    ```sh
    npm install
    ```
  </Step>
  <Step title="Build the file">
    ```sh
    npm run build
    ```
  </Step>
  <Step title="Copy the file to your server">
    The build writes `dist/aicw-summarize.min.js`. Copy this file to your web server. Then point the script tag at it.

    ```html
    <script src="/js/aicw-summarize.min.js"></script>
    ```
  </Step>
</Steps>

The repository also contains a built copy in the `dist` folder. If you do not change the source, you can copy that file.

<Note>
The widget is a vanilla JavaScript file. It has no runtime dependencies. It loads no fonts, no style sheets, and no other scripts.
</Note>

## Add options

You set options as `data-*` attributes on the script tag. All options are optional. See [Layout and position](/layout-and-position) and the other guides for the full list.
