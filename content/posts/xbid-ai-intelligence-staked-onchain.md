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

Meet [xbid.ai](https://xbid.ai) — a multi-LLM AI agent built around a simple thesis:

> Inference does not come from clever prompts alone.
> It comes from contexts encoding *a posteriori* knowledge and implicit constraints—**what we call episteme.**

Rather than relying on isolated prompt engineering, xbid.ai conditions inference on structures that embed reasoning constraints before the model generates output. This enables inference under explicit constraints rather than probabilistic guesswork.

Read the full methodology: [How We Build Better Inference](https://blog.xbid.ai/posts/xbid-ai-lab-build-better-inference/)

## Real Stake

The agent is staked. Every decision has consequences.  

The agent currently operates live markets on Stellar—executing delta-neutral strategies with AMM-hedged borrows, rebalancing collateral, and compounding recursive yield loops. This decision-loop is not limited to markets. The same architecture generalizes to competitive gaming, metaverse strategies, and other domains requiring deep causal reasoning.

## Composable by design

![Agents class diagram](/img/agents-structure.svg "Agents class diagram")

**xbid.ai** is built around composability with modular intelligence, interchangeable models, and extensible data flows.

### The model layer

A multi-LLM router fronts OpenAI, Anthropic, or any self-hosted model—so the choice of backend is orthogonal. Models can also be combined to suit strategy needs, performance, privacy, and cost profiles. For example, one model can draft the initial inference while another critiques. Our live agent works this way, blending OpenAI, Anthropic, and a fine-tuned local model (see screen).

![xbid.ai terminal](/img/xbid-terminal.png "xbid.ai terminal")

Persona behavior and build archetypes are declared in YAML (see example below), allowing models to be reshaped without refactoring. The episteme can be edited to inject feedback from past outcomes or encode temporal and causal constraints.

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
  episteme:
    description: >
      Aggressive positioning can be systematic rather than reckless.
    dialogue:
    - role: trader
      content: APY justified the leverage.
```

### The data layer

Data ingestion uses an extensible plugin system. Adapters follow one shape: fetch raw data, normalize it, distill and compute observables.

For example, the `AmmAdapter` ingests trades and pool state for Stellar constant-product pools, distillation extracts series for VWAP, volumes, and time-weighted APR. The output feeds signals.

All responses, LLM interactions, signals, and transactions are recorded for auditing and can be reused directly for feedback and epistemic refinement (see the `feedback.js` adapter for an example).

### The feedback loop

**xbid.ai** starts from the premise that inference quality depends on the context in which decisions are made. The dominant alternative assumes the opposite: that better inference can be obtained by improving instructions (prompts) in isolation.

Because cold prompts have no mechanism to accumulate, or even preserve, *a posteriori* structure, inference quickly degrades into guesswork, producing decisions that appear intelligent but lack depth or coherence.

**xbid.ai** separates feedback into two complementary paths.

- **Factual feedback.** After an action is taken, concrete outcomes such as execution costs, timing effects, utilization, concentration, and other observables, are injected directly into subsequent decisions as context.
- **Epistemic feedback.** Operating at a different level, implicit constraints and feedback are deliberately encoded into the *episteme*, altering the conditions under which future inference **begins**.

This separation allows inference to remain [grounded in reality](https://blog.xbid.ai/posts/xbid-ai-lab-build-better-inference/).

## Let's Hug

We are building xbid.ai in the open. Follow our experiments, and open-source work at [huggingface.co/xbid-labs](https://huggingface.co/xbid-labs) and [github.com/xbid-ai](https://github.com/xbid-ai). We publish code, data, and explore new approaches to reasoning systems. Contributions, feedback, and collaboration are always welcome.

Not financial advice. This is an experiment in onchain intelligence.
