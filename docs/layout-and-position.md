---
title: Layout and position
description: Set where the floating button appears, its label, and how long a closed widget stays hidden.
---

You set all options as `data-*` attributes on the script tag. This page covers the layout options.

| Attribute | Values | Default | What it does |
|-----------|--------|---------|--------------|
| `data-position` | `left`, `right`, `top`, `bottom` | `right` | Sets the edge of the page for the floating button. |
| `data-mobile-position` | `top`, `bottom`, `none` | `bottom` | Sets the position on small screens. `none` hides the widget on small screens. |
| `data-label` | text | `Summarize` | Sets the text on the button. |
| `data-remember-close-days` | number | `30` | Sets how many days a closed widget stays hidden. `0` means forever. |

If a value is not in the list of allowed values, the widget uses the default.

## Position

On the left and right edges, the button is a vertical bar at the middle of the page. On the top and bottom edges, the button is a horizontal bar at the center of the page.

This example puts the button at the bottom.

```html
<script src=""
  data-position="bottom"
></script>
```

## Small screens

A small screen is 767 pixels wide or less. On a small screen the button is a horizontal bar at the top or at the bottom. The popup is a bottom sheet. The `data-position` option does not change this.

This example hides the widget on small screens.

```html
<script src=""
  data-mobile-position="none"
></script>
```

## Label

If you do not set `data-label`, the button shows "Summarize". If you turn off the AI section and keep the share section, the button shows "Share". If you set `data-label`, the button shows your text.

This example sets a custom label.

```html
<script src=""
  data-label="Ask AI"
></script>
```

## Close button

The button has a close button (×). The popup has one too. When a visitor clicks either one, the widget hides. The widget saves the time in the browser `localStorage`, under the key `aicw-summarize-closed-until`. The widget stays hidden until the time ends.

The default time is 30 days. To change it, set `data-remember-close-days`. If the value is not a number, or is below 0, the widget uses 30.

This example hides a closed widget for 7 days.

```html
<script src=""
  data-remember-close-days="7"
></script>
```

This example hides a closed widget forever.

```html
<script src=""
  data-remember-close-days="0"
></script>
```

<Note>
If the browser blocks `localStorage`, the widget still works. It does not remember the choice.
</Note>
