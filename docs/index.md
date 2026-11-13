---
title: AICW Summarize Widget
description: A small widget that adds a floating Summarize with AI and Share button to your website.
sidebarTitle: Overview
---

The AICW Summarize Widget adds a floating button to your web pages. A visitor clicks the button and sees a small popup. The popup has links to AI services and share buttons. You add the widget with one `<script>` tag.

<Warning>
The widget does not write a summary. It opens an AI service in a new tab. The visitor then reads the summary in that service. The widget sends the page URL, the page title, and a prompt. See [How it works](/how-it-works).
</Warning>

<img src="/imgs/aicw-summarize-demo.gif" alt="Demo of the Summarize button and its popup with AI service and share icons" />

## What the widget does

- It shows a floating button on the edge of the page.
- It shows AI service links. The default services are ChatGPT, Gemini, Claude, Perplexity, and Grok.
- It shows share buttons. The default buttons are WhatsApp, Telegram, X, Gmail, and LinkedIn.
- It shows the page meta description as a preview.
- It follows the dark mode or light mode of the visitor.
- It becomes a bottom bar and a bottom sheet on small screens.

The widget has no dependencies. It does not track visitors. The widget is open source under the MIT license.

## Start here

<CardGroup cols={2}>
  <Card title="Quickstart" href="/quickstart">
    Add the widget to a page in one step.
  </Card>
  <Card title="Installation" href="/installation">
    Use the CDN, pin a release, or host the file yourself.
  </Card>
  <Card title="How it works" href="/how-it-works">
    See what the widget sends and what it does not do.
  </Card>
  <Card title="Examples" href="/examples">
    Copy a ready script tag for common cases.
  </Card>
</CardGroup>

## Live demo

To see the widget on a real site, go to [aichatwatch.com](https://aichatwatch.com). The project page is at [aichatwatch.com/summarize-widget](https://aichatwatch.com/summarize-widget/).
