---
title: How it works
description: What the widget shows, what it sends to an AI service, and what it does not do.
---

## The widget does not write summaries

The widget has no AI model and no server. It does not call any AI service. It only builds links. When a visitor clicks an AI service icon, the browser opens that service in a new tab. The AI service then writes the summary.

## What the visitor sees

1. A floating button appears on the page. The default label is "Summarize".
2. The visitor clicks the button. A popup opens.
3. The popup shows the page meta description as a "Summary" preview. This is text from your own page. If the page has no meta description, the widget uses the `og:description` tag. If the page has neither, the preview does not appear.
4. The popup shows a "Summarize with AI" row of service icons.
5. The popup shows a "Share" row of share icons.
6. The visitor clicks an icon. The service opens in a new tab.

On screens that are 767 pixels wide or less, the button becomes a bar. The popup becomes a bottom sheet.

## What the widget sends to an AI service

The link for each AI service contains one text. The text has three parts: the prompt, the page title in quotes, and the page URL. With the default prompt, the text looks like this.

```text
Summarize this page: "Page title" https://example.com/page
```

The widget puts this text in the link as a URL parameter. The AI service reads it and starts a chat. The widget sends nothing else. It does not send the page content.

The AI service may fetch the page URL itself. That is the choice of the service. It is not part of the widget.

For the list of services and their links, see [AI services and prompts](/ai-services-and-prompts).

## What the widget sends to a share service

A share link contains the page URL and, for most services, the page title. The widget adds no tracking parameters to the link. For the list of services, see [Share services](/share-services).

## Other behavior

- If the page is inside an iframe, the widget does not start.
- If a visitor clicks the close button (×), the widget hides. It stores the choice in the browser for 30 days by default. See [Layout and position](/layout-and-position).
- If you set `data-paths`, the widget shows only on matching pages. See [Show on selected pages](/show-on-selected-pages).
- If you turn off both the AI section and the share section, or the lists are empty, the widget does not appear.
