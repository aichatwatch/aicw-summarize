---
title: AI services and prompts
description: Choose the AI services in the popup and set the prompt that the widget sends.
---

The widget can show icons for seven AI services. By default it shows five. This page shows how to turn the AI section on or off, choose the services, and set the prompt.

## Options

| Attribute | Values | Default | What it does |
|-----------|--------|---------|--------------|
| `data-summarize` | `true`, `false` | `true` | Turns the AI section on or off. `0` also turns it off. |
| `data-services` | comma-separated keys | `chatgpt,gemini,claude,perplexity,grok` | Sets the services and their order. |
| `data-prompt` | text | `Summarize this page:` | Sets the prompt. Separate prompts with a vertical bar to pick one at random. |

## Services

Write the key in `data-services`. Keys are not case sensitive. The widget ignores a key that it does not know. The value `all` shows all seven services.

| Key | Service | Link that the widget opens |
|-----|---------|----------------------------|
| `chatgpt` | ChatGPT | `chat.openai.com` |
| `gemini` | Gemini | Google AI search at `google.com/search` |
| `claude` | Claude | `claude.ai/new` |
| `perplexity` | Perplexity | `perplexity.ai/search/new` |
| `grok` | Grok | Grok on X at `x.com/i/grok` |
| `deepseek` | DeepSeek | `chat.deepseek.com` |
| `copilot` | Copilot | `copilot.microsoft.com` |

Each link opens in a new tab. The widget sends the prompt, the page title, and the page URL. See [How it works](/how-it-works).

This example shows two services.

```html
<script src=""
  data-services="claude,chatgpt"
></script>
```

This example shows all seven services.

```html
<script src=""
  data-services="all"
></script>
```

## Prompt

The widget builds the text for the AI service in this order: your prompt, the page title in quotes, and the page URL. End your prompt with a colon or a similar mark, so that the title and the URL follow it in a natural way.

This example sets one prompt.

```html
<script src=""
  data-prompt="Explain this article in simple terms:"
></script>
```

## Random prompts

If you put `|` between prompts, the widget picks one prompt at random. The widget picks when it builds the popup. This happens when the page loads. It happens again if the theme changes. Empty parts are ignored.

```html
<script src=""
  data-prompt="Summarize this page:|Explain this article in simple terms:|Give me the key takeaways from:"
></script>
```

## Turn off the AI section

To show only share buttons, set `data-summarize` to `false`. See [Share services](/share-services).

```html
<script src=""
  data-summarize="false"
></script>
```
