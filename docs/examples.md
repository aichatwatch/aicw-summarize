---
title: Examples
description: Ready script tags for common cases.
---

Copy an example and change the values. Each example uses the `@latest` URL. For production, use a [pinned release](/installation).

## Minimal

This tag uses all default settings.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"></script>
```

## Custom position and label

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-position="bottom"
  data-label="Summarize"
></script>
```

## Automatic dark mode

Dark mode is automatic. You do not need to set anything. The widget reads `prefers-color-scheme` and `localStorage.theme`. To use a different `localStorage` key, set `data-theme-storage`.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-theme-storage="darkMode=true"
></script>
```

To turn off detection and always use the light colors, set `data-auto-theme` to `false`.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-auto-theme="false"
></script>
```

## Custom colors

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-auto-theme="false"
  data-bg-color="rgba(30,30,30,0.95)"
  data-text-color="#e5e7eb"
  data-accent-color="#818cf8"
  data-icon-color="#d1d5db"
  data-button-bg-color="rgba(30,30,30,0.9)"
  data-button-text-color="#e5e7eb"
></script>
```

## Random prompts

Separate the prompts with a vertical bar. The widget picks one of them.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-prompt="Summarize this page:|Explain this article in simple terms:|Give me the key takeaways from:"
></script>
```

## AI services only

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-share="false"
></script>
```

## Share buttons only

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-summarize="false"
  data-share-services="whatsapp,x,linkedin,copy"
></script>
```

## Chosen AI services and a custom prompt

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-services="claude,chatgpt"
  data-prompt="Explain this article in simple terms:"
  data-share="false"
></script>
```

## Show on selected pages

This example shows the widget only on the home page and on three top-level pages.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-paths="^/$,^/meditate/$,^/visuals/$,^/games/$"
></script>
```

This example shows the widget on all pages under `/blog/`.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-paths="^/blog/"
></script>
```

## Left side with brand colors

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-position="left"
  data-accent-color="#4f46e5"
  data-button-bg-color="#4f46e5"
  data-button-text-color="#ffffff"
></script>
```

For more detail, see [Layout and position](/layout-and-position), [Dark mode and colors](/dark-mode-and-colors), and [Show on selected pages](/show-on-selected-pages).
