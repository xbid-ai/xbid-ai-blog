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

I am honored to share that **xbid.ai** has taken **1st place** 🏆 at the [Stellar Hacks: KALE x Reflector Hackathon](https://dorahacks.io/buidl/32593/milestones) on DoraHacks! 🚀 Thank you to everyone who is backing xbid.ai at this early stage.

We are just getting started. Today I am releasing the **MCP server** for xbid.ai — tools like Claude, VS Code, or Cursor can now connect to xbid.ai and use the post-distillation pipeline data directly for inference.

{{< youtube DJWFeAxaMaM >}}

## MCP Server Release

The [Model Context Protocol](https://modelcontextprotocol.io) (MCP), often referred to as the *USB-C port* for AI, is essential infrastructure that standardizes how AI agents communicate with each other. By adopting this standard, xbid.ai can expose its pipeline and strategy engine to applications like Claude.

xbid.ai current implementation exposes only post-distillation data. This is deliberate. MCP is powerful but also increases the attack surface, for example with [tool poisoning](https://arxiv.org/abs/2508.14925), as shown by MCPTox benchmarks. It may also add latency or make atomicity harder in complex transaction scenarios. Over time, we will build additional tools that provide strategy and execution layer access — but always with strict isolation, scoped permissions, and guardrails.

Our implementation supports both `http` and `stdio` transports, check this Youtube short for a quick demo:

{{< youtube 1xgciZakC04 >}}
---

This work stands on the primitives of the Stellar ecosystem. If you want to explore them further:

 - [Stellar Developer Hub](https://developers.stellar.org)
 - [Blend Lending Protocol](https://docs.blend.capital)
 - [Reflector Oracles](https://reflector.network/docs)

Follow us and join the discussion:

 - [Youtube](https://www.youtube.com/@xbidai)
 - [X (Twitter)](https://x.com/xbid_ai)
 - [Github](https://github.com/xbid-ai)


`xbid-ai` is an ongoing experiment in onchain intelligence.

