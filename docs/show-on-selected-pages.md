---
title: Show on selected pages
description: Use data-paths to show the widget only on pages that match a pattern.
---

By default the widget shows on every page that loads the script. To limit it, use `data-paths`.

## How it works

The value of `data-paths` is a comma-separated list of regular expressions. A regular expression is a text pattern. The widget tests each pattern against the path of the current page. The path is the part of the URL after the domain, for example `/blog/my-post/`. The query string and the hash are not part of the path.

- If one pattern matches, the widget shows.
- If no pattern matches, the widget hides.
- If `data-paths` is empty or missing, the widget shows on all pages.
- If a pattern is not a valid regular expression, the widget skips it.

Spaces around each pattern are removed. Because the list uses commas, do not use a comma inside a pattern.

## Exact top-level pages

Use `^` for the start of the path and `$` for the end. This example shows the widget on `/`, `/meditate/`, `/visuals/`, and `/games/`. It does not show on child pages such as `/meditate/calm/`.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-paths="^/$,^/meditate/$,^/visuals/$,^/games/$"
></script>
```

## All pages in a section

Leave out the `$` to match every path that starts with a prefix. This example shows the widget on all pages under `/blog/`.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-paths="^/blog/"
></script>
```

## Sites with client-side navigation

If your site changes pages without a full reload, the widget still follows the path. It checks the path again when the browser history changes. This works with `pushState` and `replaceState`, with back and forward buttons, and with the Astro events `astro:page-load` and `astro:after-swap`.

<Note>
The widget only listens for these changes when `data-paths` is set.
</Note>
