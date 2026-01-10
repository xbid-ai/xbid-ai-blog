+++
title = "AI Agents Interacting with Onchain Game Markets"
date = "2025-10-17T17:00:20+09:00"
slug = "xbid-ai-agents-onchain-game-markets"
draft = false
description = ""
tags = ["blockchain", "ai", "auction house", "mcp", "stellar"]
categories = ["technology", "business", "gaming"]
authors = ["kyungjin"]
authorDisplay = ["Fred Kyung-jin Rezeau"]
[cover]
image = "/img/xbid-ai-xroads.png"
alt = "xbid.ai"
relative = false
hidden = true
+++

AI agents can now trade in-game items onchain. Last week we released the [cyberbrawl.io](https://cyberbrawl.io) auction house—a fully decentralized marketplace where players bid, offer, and execute orders for tokenized cards, heroes, and badges directly on [Stellar](https://developers.stellar.org/docs/build).

The system uses path payments to resolve prices across XLM, USDC, CREDIT, and KALE🥬 markets. Orderbooks are native Stellar ([demo](https://x.com/LitemintHQ/status/1975560243104092308)).

{{< x user="xbid_ai" id="1975560243104092308" >}}

## Cyberbrawl MCP server

To let AI agents interact with the auction house, we built an MCP server that exposes our server-side indexer. Anyone can now connect AI tools for inference and analysis. The [cyberbrawl-mcp](https://github.com/xbid-ai/cyberbrawl-mcp) server is open source.

[xbid.ai](https://xbid.ai) ingests this data to compute price movement slopes and generate trading signals. It is live on mainnet—[here is a transaction](https://stellar.expert/explorer/public/tx/2a77e8d19f7021e42f2d2a1ce31bdce64b0d44e2121cc5ea48d70e85cb05a101) where xbid.ai flipped an epic `Brawler` card for KALE🥬.

{{< youtube h7j8-2gNzNw >}}

## Games that cross boundaries

In traditional games, rare items and achievements matter to players but remain trapped in game databases. Blockchain makes them portable and verifiable—a sharable identity across experiences.

Cyberbrawl issues every card, hero, and badge onchain via Stellar. Players have been [trading them for years](https://stellar.expert/explorer/public/asset/CREDIT-GBAKUWF2HTJ325PH6VATZQ3UNTK2AGTATR43U52WQCYJ25JNSCF5OFUN-2), but through SDEX interfaces never designed for gamers. The auction house fixes this—decentralized trading embedded directly in the game.

And because everything is onchain, AI agents can participate as autonomous market makers, providing liquidity and discovering prices 24/7.

## Let's Hug

We are building xbid.ai in the open. Follow our experiments, and open-source work at [huggingface.co/xbid-labs](https://huggingface.co/xbid-labs) and [github.com/xbid-ai](https://github.com/xbid-ai). We publish code, data, and explore new approaches to reasoning systems. Contributions, feedback, and collaboration are always welcome.

Not financial advice. This is an experiment in onchain intelligence.