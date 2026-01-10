+++
title = "Fast, Native C++ BPE Token Counter for OpenAI + SentencePiece"
date = "2025-09-08T00:09:35+09:00"
slug = "cpp-openai-bpe-sentencepiece"
draft = false
description = ""
tags = ["llm", "ai", "c++", "openai", "sentencepiece"]
categories = ["technology", "business"]
authors = ["kyungjin"]
authorDisplay = ["Fred Kyung-jin Rezeau"]
[cover]
image = "https://xbid.ai/banner.png"
alt = "xbid.ai"
relative = false
hidden = true
+++

This C++ library is open source, part of the [xbid.ai](https://github.com/xbid-ai) stack. I needed a low-overhead, fast Byte Pair Encoding (BPE) counter accurate enough for billing estimates and strategy comparisons. By skipping OpenAI template overhead we trade exact parity for speed, with only ~1.5% deviation. The tool also provides support for Google's [sentencepiece](https://github.com/google/sentencepiece) binary models with a thin wrapper (100% parity).

- **C++ BPE counter** compatible with `.tiktoken` (OpenAI) encodings.
- **Quasi-parity** (no templates, <1.5% error)
- **60% faster** than OpenAI's official [tiktoken](https://www.npmjs.com/package/tiktoken) (JS/WASM)
- **No dependencies** (standard C++20 toolchain)

Our initial code was using a naive byte-length heuristic, very fast but too inaccurate. For xbid-ai, I wanted something more reliable due to the nature of our inference inputs—trading signals are unbounded, and strategy outputs are compared for costs before routing across multi-LLM/model layer.

### Benchmark (2,628 GPT-4o inputs, 16 MB)

Evaluated on a corpus of 2,628 GPT-4o requests (16.08 MB) collected directly from [xbid.ai](https://xbid.ai) live calls, with reference values from the OpenAI API usage counters.

| Method                              | Bias (tokens) | MAE  | MAPE   | R²    |
|-------------------------------------|---------------|------|--------|-------|
| Naive heuristic (n/4) | –272          | 312  | 10.6%  | 0.889 |
| Native C++ BPE Counter (xbid.ai)    | –12           | 12   | 1.48%  | 1.0   |

Reducing error from ~10% to ~1.5% while remaining fast and lightweight.

### IPC server mode

The tool provides a tiny IPC server so you can preload models, keep it alive and stream requests over stdin/stdout. Especially useful for high-throughput or multi-LLM pipelines, to avoid the overhead of spawning a new process per request.

xbid.ai uses this mode and you can find our client implementation in the [xbid-ai](https://github.com/xbid-ai/xbid-ai) repo.

```bash
# OpenAI BPE
./tokkit --provider openai --model /data/o200k_base.tiktoken --serve

# SentencePiece (built with -DSENTENCEPIECE=1)
./tokkit --provider sentencepiece --model /data/tokenizer.model --serve
```

---

### Open source

This work is [open source](https://github.com/xbid-ai/xbid-ai-tokkit) under the MIT license. Pull requests, issues, and discussions are always welcome.

If you want to explore further:

- [SentencePiece](https://github.com/google/sentencepiece) — Google tokenizer library.
- [OpenAI tiktoken](https://github.com/openai/tiktoken) — official tokenizer for GPT models

**Note** The *best place* to find SentencePiece models (`.model`) is [Hugging Face](https://huggingface.co) model hub.

## Let's Hug

We are building xbid.ai in the open. Follow our experiments, and open-source work at [huggingface.co/xbid-labs](https://huggingface.co/xbid-labs) and [github.com/xbid-ai](https://github.com/xbid-ai). We publish code, data, and explore new approaches to reasoning systems. Contributions, feedback, and collaboration are always welcome.

Not financial advice. This is an experiment in onchain intelligence.
