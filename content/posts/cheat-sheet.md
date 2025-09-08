+++
title = "Cheat Sheet"
date = "2025-08-16T23:26:16+09:00"  # quoted to avoid TOML parser ambiguity
draft = true
private = true
description = "Reference post for formatting, code, images, video, social embeds, quotes, tables."
tags = ["reference", "hugo", "papermod"]
categories = ["docs"]

[cover]
image = "https://xbid.ai/banner.png"
alt = "xbid.ai"
caption = "xbid.ai - Intelligence. Staked. Onchain."
+++

> Reference for how to format rich content on **blog.xbid.ai** using Hugo + PaperMod.

## Headings, emphasis, lists

- **Bold**, *italic*, `inline code`
- Ordered:
  1. First
  2. Second

---

## Images (Markdown)

![Alt text](/img/cover.png "image title")

## Images (figure shortcode with caption)

{{< figure src="/img/cover.png" alt="Cover" title="Cover image" caption="Figure: xbid.ai cover" >}}

## Code blocks (JS + Shell) with line numbers and highlights

```js {linenos=true,hl_lines=[2]}
export function analyze(delta) {
  if (delta.apy > 0.1) {
    return { action: "allocate", weight: 0.7 };
  } else {
    return { action: "hold", weight: 0.3 };
  }
}
```

```bash {linenos=table}
hugo version
hugo server -D
hugo --minify
```

## YouTube

{{< youtube j9k61KUxjF8 >}}

## Vimeo

{{< vimeo 777147453 >}}

## Instagram

{{< instagram DFepDclxdeu >}}

## X (Twitter) post

{{< x user="xbid_ai" id="1962784481707991482" >}}

## HTML5 Video (self-hosted)

{{< video src="/videos/demo.mp4" poster="/images/cover.png" width="800" >}}

## Blockquote, table

> Markets are a mirror. They do not care; they only reflect.

| metric      | value |
|-------------|-------|
| apy         | 5.7%  |
| utilization | 63%   |
| q4w         | 0.12  |

## Internal links

See the [About](/about/) page and the [Posts](/posts/) list.
