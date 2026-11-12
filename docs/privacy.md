---
title: Privacy
description: What the widget stores, what it sends, and what happens when a visitor clicks an icon.
---

The widget has no tracking and no analytics. This page lists what the code does, so that you can describe it in your own privacy policy.

## Network requests

The widget makes no network requests of its own. It loads no fonts, no style sheets, and no other scripts. All icons are inline SVG images in the script file. The widget sends no data to AI Chat Watch (AICW) or to any other server.

The only request for the widget file is the one your page makes to load it. If you use the jsDelivr CDN, jsDelivr receives that request. To avoid this, [host the file yourself](/installation).

## What the widget stores in the browser

| Key in `localStorage` | When | Purpose |
|-----------------------|------|---------|
| `aicw-summarize-closed-until` | A visitor closes the widget | Keeps the widget hidden until the time ends. |

The widget also reads the `localStorage` key that you set in `data-theme-storage` (default `theme`). It only reads this key, to find out if the site uses dark mode. It does not write to it. It does not set cookies.

## What happens when a visitor clicks an icon

The widget does not send data on its own. The visitor leaves your page for another service only when they click an icon.

- **AI service icon.** A new tab opens at the AI service. The link contains the prompt, the page title, and the page URL. From then on, the privacy policy of that service applies.
- **Share icon.** A new tab opens at the share service, or the email program opens. The link contains the page URL and, for most services, the page title. The policy of that service applies.
- **Copy link icon.** The widget copies the page URL to the clipboard. Nothing leaves the page.

The widget adds no tracking parameters to these links.

## What the widget reads from the page

- The page URL and the page title, to build the links.
- The meta description, or the `og:description` tag, to show the preview. The preview text comes from your own page.

<Note>
This page describes the widget code. It is not legal advice. If you use the widget, check that your own privacy policy covers the links that visitors can open.
</Note>

For the policy of AI Chat Watch (AICW), see the [privacy page on aichatwatch.com](https://aichatwatch.com/privacy/).
