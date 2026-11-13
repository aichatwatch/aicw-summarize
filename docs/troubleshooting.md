---
title: Troubleshooting
description: Fix common problems with the Summarize widget.
---

## The button does not appear

Check each item in this list.

- **The script tag is missing or the URL is wrong.** Open the browser developer tools. Look at the Network tab for a failed request to `aicw-summarize.min.js`.
- **The widget was closed.** If a visitor or you clicked the close button, the widget stays hidden. By default it stays hidden for 30 days. To show it again, delete the `aicw-summarize-closed-until` key in the browser `localStorage`.
- **`data-paths` does not match.** The widget only shows on matching paths. See [Show on selected pages](/show-on-selected-pages).
- **Both sections are empty.** If `data-summarize` and `data-share` are `false`, or if every service key is wrong, the widget does not start. Check the spelling of the keys.
- **Small screen.** If `data-mobile-position` is `none`, the widget hides on screens that are 767 pixels wide or less.
- **The page is in an iframe.** The widget does not start inside an iframe.

## A service icon is missing

The widget ignores a service key that it does not know. Check the spelling in `data-services` or `data-share-services`. See [AI services and prompts](/ai-services-and-prompts) and [Share services](/share-services) for the valid keys.

## The widget uses the wrong theme

Check these items.

- If `data-auto-theme` is `false`, the widget always uses light colors.
- If your site stores its theme in `localStorage`, set `data-theme-storage` to the right key and dark value, for example `darkMode=true`.
- If the key exists but the value is not the dark value, the widget uses light mode. It does not look at the browser setting.

See [Dark mode and colors](/dark-mode-and-colors).

## A color does not change

The widget ignores a color that the browser does not accept. Use a valid CSS color, for example `#4f46e5`. A value with `;`, `{`, or `}`, or one that is longer than 80 characters, is ignored.

## The AI service does not show a summary

The widget only opens the AI service. The service decides what it does with the link. Some services may ask the visitor to sign in first. Some services may not read the page. These behaviors are outside the widget. See [How it works](/how-it-works).

## The summary preview is missing

The preview comes from the meta description of the page. If the page has no `description` meta tag and no `og:description` tag, the widget shows no preview. Add one of these tags to your page.

## Report a problem

To report a bug or ask a question, open an issue on [GitHub](https://github.com/aichatwatch/aicw-summarize/issues). For other contact, use [aichatwatch.com/quote](https://aichatwatch.com/quote).
