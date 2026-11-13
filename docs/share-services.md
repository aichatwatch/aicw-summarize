---
title: Share services
description: Choose the share buttons in the popup.
---

The popup has a "Share" row. It has five buttons by default. You can choose from twelve.

## Options

| Attribute | Values | Default | What it does |
|-----------|--------|---------|--------------|
| `data-share` | `true`, `false` | `true` | Turns the share section on or off. `0` also turns it off. |
| `data-share-services` | comma-separated keys | `whatsapp,telegram,x,gmail,linkedin` | Sets the buttons and their order. |

Keys are not case sensitive. The widget ignores a key that it does not know. The value `all` shows all twelve buttons.

## Services

| Key | Service | What happens on click |
|-----|---------|-----------------------|
| `whatsapp` | WhatsApp | Opens WhatsApp with the title and the URL. |
| `x` | X (Twitter) | Opens the X post form with the title and the URL. |
| `telegram` | Telegram | Opens Telegram share with the URL and the title. |
| `facebook` | Facebook | Opens the Facebook sharer with the URL. |
| `linkedin` | LinkedIn | Opens LinkedIn share with the URL. |
| `reddit` | Reddit | Opens the Reddit submit form with the URL and the title. |
| `threads` | Threads | Opens the Threads post form with the title and the URL. |
| `bluesky` | Bluesky | Opens the Bluesky compose form with the title and the URL. |
| `mastodon` | Mastodon | Opens a Mastodon share page with the title and the URL. |
| `gmail` | Gmail | Opens a Gmail draft with the title as subject and the URL in the body. |
| `email` | Email | Opens your email program with the title as subject and the URL in the body. |
| `copy` | Copy link | Copies the page URL to the clipboard. The icon shows a check mark for a short time. |

All services except `copy` open in a new tab. The `copy` button does not leave the page.

## Examples

This example shows four buttons.

```html
<script src=""
  data-share-services="whatsapp,x,linkedin,copy"
></script>
```

This example shows AI services only. It turns off the share section.

```html
<script src=""
  data-share="false"
></script>
```

This example shows share buttons only.

```html
<script src=""
  data-summarize="false"
  data-share-services="whatsapp,x,linkedin,copy"
></script>
```

If you turn off the AI section, the button label is "Share" unless you set `data-label`.
