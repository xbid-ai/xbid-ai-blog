# xbid.ai Blog

Repo for [blog.xbid.ai](https://blog.xbid.ai) blog.

xbid.ai is an open experiment in onchain intelligence. Our blog shares raw design notes, experiments, results (good and bad), code, walkthroughs, and the latest developments. 

## Quick Start

**Contributors:** Please follow the steps below to set up, create posts. Once your changes are ready, [open a pull request](https://github.com/xbid-ai/xbid-ai-blog/pulls) so they can be reviewed, merged, and published.

### Dev server (with drafts)
```bash
hugo server -D
```
Serves on `http://localhost:1313`

### New post
```bash
hugo new posts/your-post-slug.md
```
Then edit the front matter and body. We use TOML front matter with consistent taxonomies and author fields, here is an example:

```toml
+++
title = "Post Title"
date = "2026-01-01T00:09:35+09:00"
slug = "your-post-slug"
draft = false
description = "One-liner summary"
tags = ["ai", "c++"]
categories = ["technology"]
authors = ["kyungjin"]
authorDisplay = ["Fred Kyung-jin Rezeau"]
[cover]
image = "https://xbid.ai/banner.png"
alt = "xbid.ai"
relative = false
hidden = false
+++
```

**Formatting rules**
For consistency, please follow the formatting guidelines in our [Cheat Sheet](https://github.com/xbid-ai/xbid-ai-blog/blob/main/content/posts/cheat-sheet.md).  
It covers headings, emphasis, lists, code blocks, images, videos, social embeds, quotes, and tables.

### Publish (production build)
```bash
hugo --gc --minify
```
Deploy by uploading the **contents** of `public/` to host.

## Taxonomies & Authors

- **Authors**: Each contributor should add themselves under `content/authors/<handle>/_index.md`. See `content/authors/kyungjin/_index.md` as an example.
- **Tags**: granular topics (e.g. `llm`, `openai`, `c++`).
- **Categories**: higher-level groupings (e.g. `technology`, `business`).