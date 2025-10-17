+++
title = "At the Crossroad of AI, Gaming, and Blockchain"
date = "2025-10-17T17:00:20+09:00"
slug = "xbid-ai-crossroad-gaming-blockchain"
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

We released the [cyberbrawl.io](https://cyberbrawl.io) auction house (AH) last week. The AH is fully decentralized, allows trading in-game items (cards, heroes, badges), and is built directly on [Stellar](https://developers.stellar.org/docs/build). Right from within the game, players can place bids, offers, and execute buy and sell orders across markets for every tokenized game item.

The system uses path payments to resolve prices across markets — XLM, USDC, CREDIT, KALE🥬. The orderbooks are native (see our [X.com](https://x.com/LitemintHQ/status/1975560243104092308) video demo below).

{{< x user="xbid_ai" id="1975560243104092308" >}}

## Cyberbrawl MCP server

To extend the utility, I also built an MCP server to expose the cyberbrawl server-side indexer service, letting anyone connect their own AI tools for inference and opportunity discovery. The [cyberbrawl-mcp](https://github.com/xbid-ai/cyberbrawl-mcp) server is open source.

{{< youtube h7j8-2gNzNw >}}

Additionally, [xbid.ai]() was instrumented to ingest the indexed data, allowing the pipeline to compute the slope of price movements and derive flip signals for its spot strategy. It's live, currently executing on mainnet. Check out [this transaction](https://stellar.expert/explorer/public/tx/2a77e8d19f7021e42f2d2a1ce31bdce64b0d44e2121cc5ea48d70e85cb05a101), xbid.ai flipping the epic `Brawler` card to get more KALE🥬.


## Games that cross boundaries

{{< youtube bI_BUNgN344 >}}

In traditional games, achievements, titles, and rare items represent players skills and markers of identity. They matter a lot to players, but remain stuck in the game databases. As discussed in the video above, blockchain shifts that. We can improve player experience with decentralized proof of ownership, achievements and items become portable, verifiable across experiences — a sharable identity.

This is why cyberbrawl.io issues every card, hero, and badge directly onchain, on Stellar. Players have been trading them for [years already](https://stellar.expert/explorer/public/asset/CREDIT-GBAKUWF2HTJ325PH6VATZQ3UNTK2AGTATR43U52WQCYJ25JNSCF5OFUN-2), but through SDEX interfaces never designed for gamers. The new **auction house** in cyberbrawl.io fixes this. We offer a fully decentralized marketplace, embedded directly in cyberbrawl.io, where bidding and trading is seamless.

xbid.ai sits at the crossroad of these layers. It leverages all markets seamlessly —spot trading, lending, hedging, flipping in-game items, crossing the boundaries as if they never existed. That is the power of blockchain and AI together.

Follow us and join the discussion:

 - [Youtube](https://www.youtube.com/@xbidai)
 - [X (Twitter)](https://x.com/xbid_ai)
 - [Github](https://github.com/xbid-ai)


`xbid-ai` is an ongoing experiment in onchain intelligence.