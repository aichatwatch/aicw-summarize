---
title: Dark mode and colors
description: How the widget picks light or dark colors, and how to set your own colors.
---

The widget picks a light or dark color set on its own. You can turn this off. You can also set each color.

## Options for dark mode

| Attribute | Values | Default | What it does |
|-----------|--------|---------|--------------|
| `data-auto-theme` | `true`, `false` | `true` | Turns automatic dark mode on or off. `0` also turns it off. |
| `data-theme-storage` | `varName=darkValue` or `none` | `theme=dark` | Names the `localStorage` key and the value that mean dark mode. |

## How detection works

1. The widget reads the `localStorage` key from `data-theme-storage`. The default key is `theme`.
2. If the key has a value, the widget uses dark mode when the value equals the dark value (`dark` by default). Any other value gives light mode.
3. If the key has no value, or `data-theme-storage` is `none`, the widget uses the browser setting `prefers-color-scheme`.
4. The widget watches for changes. If the browser setting or the stored value changes, the widget updates its colors at once.

If `data-auto-theme` is `false`, the widget always uses the light colors.

This example uses a different `localStorage` key. The widget uses dark mode when `darkMode` equals `true`.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-theme-storage="darkMode=true"
></script>
```

This example ignores `localStorage` and follows the browser setting only.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-theme-storage="none"
></script>
```

This example turns off automatic detection.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-auto-theme="false"
></script>
```

## Built-in colors

| Part | Light mode | Dark mode |
|------|------------|-----------|
| Popup background | `#ffffff` | `#1f2937` |
| Text | `#374151` | `#e5e7eb` |
| Icons | `#1f2937` | `#d1d5db` |
| Button background | `#ffffff` | `#111827` |
| Button text | same as text | `#e5e7eb` |
| Accent | same as text | `#818cf8` |

## Set your own colors

An explicit color attribute replaces the automatic color. Use these when you need to match your brand.

| Attribute | What it sets |
|-----------|--------------|
| `data-bg-color` | Popup background |
| `data-text-color` | Text in the popup |
| `data-accent-color` | Accent gradient on the edge of the button and the popup |
| `data-icon-color` | Icon color |
| `data-button-bg-color` | Button background |
| `data-button-text-color` | Button text |

Each value must be a valid CSS color, such as `#4f46e5` or `rgba(30,30,30,0.95)`. The widget ignores a value that the browser does not accept, or one that is longer than 80 characters. For the accent color, use a hex value such as `#4f46e5`. The widget builds the accent gradient from a hex value.

This example sets all six colors for a dark look.

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

This example uses brand colors on the left edge.

```html
<script src="https://cdn.jsdelivr.net/gh/aichatwatch/aicw-summarize@latest/dist/aicw-summarize.min.js"
  data-position="left"
  data-accent-color="#4f46e5"
  data-button-bg-color="#4f46e5"
  data-button-text-color="#ffffff"
></script>
```
