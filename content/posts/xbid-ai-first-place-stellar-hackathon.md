+++
title = "xbid.ai Wins 1st Place at Stellar Hacks + MCP Server Released"
date = "2025-09-15T17:00:20+09:00"
slug = "xbid-ai-first-place-stellar-hackathon"
draft = false
description = ""
tags = ["hackathon", "ai", "mcp", "stellar"]
categories = ["technology", "business"]
authors = ["kyungjin"]
authorDisplay = ["Fred Kyung-jin Rezeau"]
[cover]
image = "https://xbid.ai/banner.png"
alt = "xbid.ai"
relative = false
hidden = true
+++

**xbid.ai won 1st place** 🏆 at the [Stellar Hacks: KALE x Reflector Hackathon](https://dorahacks.io/buidl/32593/milestones) on DoraHacks! 🚀 Thanks to everyone backing this early.

To celebrate, I am releasing the **MCP server** for xbid.ai—tools like Claude, VS Code, and Cursor can now connect to xbid.ai and use post-distillation pipeline data for inference.

{{< youtube DJWFeAxaMaM >}}

## MCP Server Release

The [Model Context Protocol](https://modelcontextprotocol.io) (MCP), often referred to as the *USB-C port* for AI, is essential infrastructure that standardizes how AI agents communicate with each other. By adopting this standard, xbid.ai can expose its pipeline and strategy engine to applications like Claude.

xbid.ai current implementation exposes only post-distillation data. It is deliberately scoped to minimize attack surface. MCP is powerful but introduces latency and risks like [tool poisoning](https://arxiv.org/abs/2508.14925), or make atomicity harder in complex transaction scenarios. Over time, we will build additional tools that provide scoped visibility into strategy and execution layers — but always with strict isolation, scoped permissions, and guardrails.

Our implementation supports both `http` and `stdio` transports. Quick demo:

{{< youtube 1xgciZakC04 >}}
---

This work stands on the primitives of the Stellar ecosystem. If you want to explore them further:

 - [Stellar Developer Hub](https://developers.stellar.org)
 - [Blend Lending Protocol](https://docs.blend.capital)
 - [Reflector Oracles](https://reflector.network/docs)

## Let's Hug

We are building xbid.ai in the open. Follow our experiments, and open-source work at [huggingface.co/xbid-labs](https://huggingface.co/xbid-labs) and [github.com/xbid-ai](https://github.com/xbid-ai). We publish code, data, and explore new approaches to reasoning systems. Contributions, feedback, and collaboration are always welcome.

Not financial advice. This is an experiment in onchain intelligence.
