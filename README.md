<div align="center">

# Tremayne Timms

**ML & AI Engineer** — Fine-Tuning · Agentic Systems · Edge Deployment · Production LLM Ops

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tremayne-t-/)
[![GitHub followers](https://img.shields.io/github/followers/t-timms?style=flat-square&logo=github&label=Follow&color=2f80ed)](https://github.com/t-timms)
[![GitHub stars](https://img.shields.io/github/stars/t-timms?style=flat-square&logo=github&label=Stars&color=2f80ed)](https://github.com/t-timms?tab=repositories)

</div>

---

## About Me

I build production LLM systems from the metal up — from quantized models running on Jetson edge hardware to multi-agent cloud deployments with tool-use, permission gating, and audit trails. Currently focused on MoE fine-tuning, Blackwell-native FP4 quantization (NVFP4), and SOTA agentic coding benchmarks.

Dallas-Fort Worth, TX · [ttimmsinternational@gmail.com](mailto:ttimmsinternational@gmail.com)

[![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Rust](https://img.shields.io/badge/-Rust-000000?style=flat-square&logo=rust&logoColor=white)](https://rust-lang.org)
[![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://typescriptlang.org)
[![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org)
[![CUDA](https://img.shields.io/badge/-CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)](https://developer.nvidia.com/cuda-zone)
[![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://docker.com)
[![GitHub Actions](https://img.shields.io/badge/-GitHub%20Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)](https://github.com/features/actions)
[![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://postgresql.org)

---

## Current Focus (July 2026)

| Project | What | Why It Matters |
|---------|------|----------------|
| **[zaya1-godspeed](https://github.com/t-timms/zaya1-godspeed)** | NVFP4 W4A4 (4-bit weights *and* activations) serving for ZAYA1-8B MoE on consumer Blackwell SM120 | Custom vLLM CUTLASS source build — **102.6 tok/s single / 407 tok/s batch-8** in <6 GB VRAM on RTX 5070 Ti, plus s1-style budget-forced reasoning evals proving the checkpoint healthy (GPQA-Diamond 45.8% → 62.5% with reasoning budget) |
| **[llama.cpp NVFP4](https://github.com/t-timms/llama.cpp-nvfp4)** | Blackwell-native FP4 quantization with MSE-optimal scales | First consumer NVFP4 tooling on RTX 5070 Ti — [PR #22897](https://github.com/ggml-org/llama.cpp/pull/22897) awaiting upstream review |

---

## What I'm Building

### [ZAYA1 NVFP4 W4A4 on Blackwell](https://github.com/t-timms/zaya1-godspeed)

End-to-end NVFP4 W4A4 quantization + serving for Zyphra's ZAYA1-8B (80-layer MoE + CCA attention) on a 16 GB RTX 5070 Ti. Rebuilt vLLM from source with SM120 CUTLASS FP4 kernels, wrote the layer-wise activation calibration, reverse-engineered the NVFP4 global-scale convention, and built budget-forced eval harnesses for reasoning models. 102.6 tok/s single-stream, 407.4 tok/s batch-8, 5.99 GB checkpoint.

### [Godspeed Coding Agent](https://github.com/t-timms/godspeed-coding-agent) [![CI](https://img.shields.io/github/actions/workflow/status/t-timms/godspeed-coding-agent/ci.yml?style=flat-square&label=CI)](https://github.com/t-timms/godspeed-coding-agent/actions/workflows/ci.yml) [![Coverage](https://img.shields.io/badge/coverage-81%25-success?style=flat-square)](https://github.com/t-timms/godspeed-coding-agent)

Security-first open-source coding agent. Hand-rolled async ReAct loop with 4-tier deny-first permission engine, SHA-256 hash-chained audit trail, and 200+ LLM providers via LiteLLM. 4,600+ tests.

- 30+ built-in tools with JSON Schema validation, MCP server + client
- Parallel + speculative tool dispatch, cost budget enforcement
- Self-evolution via LLM-guided mutations, multi-language verify gate with retry
- Training data export (openai/chatml/sharegpt), per-step reward annotations for GRPO
- **SWE-bench Lite: 34.8% single-shot · 52.2% oracle best-of-5**

### [Sovereign Edge](https://github.com/t-timms/sovereign-edge)

Autonomous multi-agent personal intelligence system on NVIDIA Jetson Orin Nano. 5 LangGraph expert agents, LiteLLM gateway (4 providers + Ollama), 3-tier ONNX intent router. 393 tests. Fully on-device — zero cloud dependencies.

### [Manna Trading](https://github.com/t-timms/manna-trading)

Multi-agent algorithmic trading pipeline with DeepSeek R1 reasoning at every stage. 4-agent pipeline (TA → Chief → Risk → Execution), Kelly Criterion position sizing, Monte Carlo risk simulation, real-time WebSocket market data.

### [Bible AI Assistant](https://github.com/t-timms/bible-ai-assistant)

Qwen3.5-4B fine-tuned with ORPO for biblical Q&A. Hybrid RAG (ChromaDB + BM25 + cross-encoder reranking), constitutional AI guardrails, voice pipeline (Whisper + Kokoro TTS), Gradio UI. 183 tests, 34 W&B runs, 5,925 training steps.

### [GPU Server Test Suite](https://github.com/t-timms/gpu-server-test-suite)

Comprehensive GPU fleet validation modeled on NVIDIA DCGM. 16 diagnostic modules, Prometheus + Grafana, fault injection, JUnit XML for CI. 188 tests.

### [ML Lab](https://github.com/t-timms/ml-lab)

ML research control plane — experiment lifecycle management, model registry, cloud training launcher. Orchestrates gpu-server-test-suite (preflight checks) and llm-wiki (knowledge persistence). 28 tests, v0.1.0.

### [LLM Wiki](https://github.com/t-timms/llm-wiki)

Git-backed knowledge base — Karpathy's LLM Wiki pattern. LangGraph ingest/query pipelines, instructor + Pydantic structured output, BM25 search, Groq → Gemini → Ollama fallback via LiteLLM. 117 tests, 40 wiki pages.

### [Manufacturing Quality Analytics](https://github.com/t-timms/manufacturing-quality-analytics)

SQL + Python ETL pipeline for semiconductor quality analysis — supplier performance scoring, defect Pareto distributions, yield trend analysis.

### [Tesla Tire Wear ML](https://github.com/t-timms/tesla-tire-wear-ml)

Multi-model ML pipeline for Tesla tire wear prediction. Random Forest, XGBoost, Neural Network ensemble with Claude AI integration.

---

## Open Source Contributions

- **[llama.cpp #22897](https://github.com/ggml-org/llama.cpp/pull/22897)** — NVFP4 default type mapping + per-tensor scale tensors + MSE-optimal correction
- **[llama.cpp #22858](https://github.com/ggml-org/llama.cpp/pull/22858)** — Missing `LLAMA_FTYPE_MOSTLY_NVFP4` case fix (closed, replaced by #22897)

---

## GitHub Activity

<div align="center">
  <picture>
    <source
      srcset="https://github-readme-stats.vercel.app/api?username=t-timms&show_icons=true&include_all_commits=true&count_private=true&theme=github_dark&hide_border=true&title_color=2f80ed&icon_color=2f80ed"
      media="(prefers-color-scheme: dark)"
    />
    <source
      srcset="https://github-readme-stats.vercel.app/api?username=t-timms&show_icons=true&include_all_commits=true&count_private=true&theme=default&hide_border=true"
      media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
    />
    <img height="180" src="https://github-readme-stats.vercel.app/api?username=t-timms&show_icons=true&include_all_commits=true&count_private=true&theme=default&hide_border=true" />
  </picture>
  <picture>
    <source
      srcset="https://github-readme-stats.vercel.app/api/top-langs?username=t-timms&layout=compact&langs_count=8&theme=github_dark&hide_border=true&title_color=2f80ed&text_color=8b949e"
      media="(prefers-color-scheme: dark)"
    />
    <source
      srcset="https://github-readme-stats.vercel.app/api/top-langs?username=t-timms&layout=compact&langs_count=8&theme=default&hide_border=true"
      media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
    />
    <img height="180" src="https://github-readme-stats.vercel.app/api/top-langs?username=t-timms&layout=compact&langs_count=8&theme=default&hide_border=true" />
  </picture>
  <br />
  <picture>
    <source
      srcset="https://streak-stats.demolab.com/?user=t-timms&theme=github-dark-blue&hide_border=true"
      media="(prefers-color-scheme: dark)"
    />
    <source
      srcset="https://streak-stats.demolab.com/?user=t-timms&theme=default&hide_border=true"
      media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
    />
    <img height="180" src="https://streak-stats.demolab.com/?user=t-timms&theme=default&hide_border=true" />
  </picture>
</div>

<details>
  <summary><b>📈 Contribution Graph</b></summary>
  <br />
  <picture>
    <source
      srcset="https://github-readme-activity-graph.vercel.app/graph?username=t-timms&theme=react-dark&hide_border=true&area=true"
      media="(prefers-color-scheme: dark)"
    />
    <source
      srcset="https://github-readme-activity-graph.vercel.app/graph?username=t-timms&theme=github-light&hide_border=true&area=true"
      media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
    />
    <img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=t-timms&theme=react-dark&hide_border=true&area=true" />
  </picture>
</details>

---

## Skills

| Area | Technologies |
|------|-------------|
| **LLMs & Agents** | LiteLLM, 200+ providers, Ollama, llama.cpp, multi-agent orchestration, ReAct loops |
| **Fine-Tuning** | Unsloth, TRL (SFT/DPO/GRPO/ORPO), QLoRA, PEFT, MoE architectures, RLHF/RLAIF |
| **Inference** | vLLM (custom forks), speculative decoding (750 tok/s), TensorRT-LLM, EXL2 |
| **Quantization** | NVFP4 (Blackwell-native), GGUF, EXL2, FP8, NF4, GPTQ, AWQ |
| **ML Infrastructure** | PyTorch, CUDA 12.8, torch.compile, DeepSpeed, lm-eval, W&B, MLflow |
| **Systems** | Python, Rust, TypeScript, Docker, GitHub Actions CI/CD, systemd |
| **Edge / Hardware** | NVIDIA Jetson Orin Nano, RTX 5070 Ti (Blackwell sm_120), 16 GB VRAM optimization |
| **Data** | PostgreSQL, SQL, pandas, SQLAlchemy, ChromaDB, LanceDB, BM25 |

---

<div align="center">

**Tremayne Timms** · [GitHub](https://github.com/t-timms) · [LinkedIn](https://www.linkedin.com/in/tremayne-t-/) · [Email](mailto:ttimmsinternational@gmail.com)

</div>
