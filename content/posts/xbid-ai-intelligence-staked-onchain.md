+++
title = "xbid.ai — intelligence. staked. onchain."
date = "2025-08-27T00:00:00+01:00"
slug = "xbid-ai-intelligence-staked-onchain"
draft = false
description = ""
tags = ["llm", "ai", "agent", "welcome"]
categories = ["technology", "business"]
authors = ["kyungjin"]
authorDisplay = ["Fred Kyung-jin Rezeau"]
[cover]
image = "https://xbid.ai/banner.png"
alt = "xbid.ai"
relative = false
hidden = true
+++

Meet [xbid.ai](https://xbid.ai) — a multi-LLM AI agent born on Stellar, built to evolve and roam anywhere.

With real stake and a memory of outcomes, selection pressure shapes behavior. **xbid.ai** is an open experiment built on that premise. **The vision** is simple: create an intelligence that carries its own weight and evolves by owning what it does.

Whether trading for carry, running NFT auctions, gaming competitively, or participating in metaverse and web3 activities, the same loop can be applied where reinforcement routes receipts back into behavior, holding the agent to outcomes.

---

## Built to evolve

![Agents class diagram](/img/agents-structure.svg "Agents class diagram")

**xbid.ai** is built to evolve: intelligence and environment are modular, models can interact, and data flows can be extended without friction.

### The model layer

A multi-LLM router fronts OpenAI, Anthropic, or any self-hosted model—so the choice of backend is orthogonal. Models can also be combined to suit strategy needs, performance, privacy, and cost profiles. For example, one model can draft the initial inference while another critiques. Our live agent works this way, blending OpenAI, Anthropic, and a fine-tuned local model (see screen).

![xbid.ai terminal](/img/xbid-terminal.png "xbid.ai terminal")

Persona behavior and build archetypes are declared in YAML (see example below), allowing models to be reshaped without refactoring.

```yaml
trader:
  provider: openai
  model: gpt-4o
  archetype: degen trader
  role: |
    As an autonomous trading intelligence, you are managing a live on-chain...
  traits:
    - You act with confidence and precision.
    - You are creative
  rules:
    - Allow yourself to take risks.
    - Prefer profit maximizing strategies.
```

### The data layer

Data ingestion uses an extensible plugin system. Adapters follow one shape: fetch raw data, normalize it, distill and compute observables.

For example, the `AmmAdapter` ingests trades and pool state for Stellar constant-product pools, distillation extracts series for VWAP, volumes, and time-weighted APR. The output feeds signals.

All responses, LLM interactions, signals, and transactions are recorded for auditing and can be reused directly in self-feedback loops (see the `feedback.js` adapter for an example).

## The feedback loop

At its core, **xbid.ai** is designed to be driven by selection pressure. 

The initial idea came from a conversation I had with ChatGPT about the small disclaimer under the chat box that 'GPT can make mistakes.' We ended up talking about what it would take to make an AI accountable and drifted into a future where AI might spawn short-lived blockchain networks, created on the fly to serve situational needs, then dissolved after transacting with other agents.

![ChatGPT disclaimer](/img/chatgpt-disclaimer.png "ChatGPT disclaimer")

Most systems stop at automation or backtesting. The idea with **xbid.ai**'s multi-LLM agent is to push further, treating markets, outcomes, and even crowd input as the environment applying pressure on the agent. Every trade, every decision, every outcome feeds back into behavior, shaping what survives.

The **ai lab** is where this open loop executes. It offers free to join, no deposits, daily experiments, challenges, and gamified activities that let participants reinforce or contest outcomes in real time.


## Watch the loop in motion

This blog shares the xbid.ai journey — design notes, experiments, results, upcoming features, plus videos and walkthroughs.

If you want to grab signals, alphas, contribute to reinforcement, open the terminal at [https://xbid.ai](https://xbid.ai).

 If you want to mirror or extend the system, [fork it](https://github.com/xbid-ai/xbid-ai) and go. The code is MIT‑licensed, issues and PRs welcome.

Not financial advice. This is an experiment in onchain intelligence.
