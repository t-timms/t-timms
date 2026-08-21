<div align="center">

# Tremayne Timms

**ML & AI Engineer** — Fine-Tuning · Agentic Systems · Edge Deployment · Production LLM Ops

Dallas-Fort Worth, TX · [ttimmsinternational@gmail.com](mailto:ttimmsinternational@gmail.com) · [Portfolio](https://t-timms.github.io)

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tremayne-t-/)
[![GitHub followers](https://img.shields.io/github/followers/t-timms?style=flat-square&logo=github&label=Follow&color=2f80ed)](https://github.com/t-timms)

<br>

<picture>
  <source srcset="https://skillicons.dev/icons?i=python%2Cts%2Cpytorch%2Cdocker%2Cgithubactions%2Cpostgres&theme=dark" media="(prefers-color-scheme: dark)" />
  <source srcset="https://skillicons.dev/icons?i=python%2Cts%2Cpytorch%2Cdocker%2Cgithubactions%2Cpostgres" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)" />
  <img src="https://skillicons.dev/icons?i=python%2Cts%2Cpytorch%2Cdocker%2Cgithubactions%2Cpostgres" alt="Python, TypeScript, PyTorch, Docker, GitHub Actions, PostgreSQL" />
</picture>

</div>

---

## Highlights

[![SWE-bench Lite](https://img.shields.io/badge/SWE--bench_Lite-34.8%25_single--shot_·_52.2%25_oracle_b5-2f80ed?style=flat-square)](https://github.com/t-timms/godspeed-coding-agent#benchmarks)
[![NVFP4 W4A4](https://img.shields.io/badge/NVFP4_W4A4_serving-9.5_tok%2Fs_·_~74_batch--8-2f80ed?style=flat-square)](https://github.com/t-timms/zaya1-godspeed)
[![Speculative decoding](https://img.shields.io/badge/n--gram_spec_decode-2.2×_validated-2f80ed?style=flat-square)](https://github.com/t-timms/zaya1-godspeed)
[![Tests](https://img.shields.io/badge/tests_across_projects-5%2C500%2B_passing-2f80ed?style=flat-square)](https://github.com/t-timms/godspeed-coding-agent)
[![Upstream](https://img.shields.io/badge/llama.cpp-NVFP4_PR_open_upstream-2f80ed?style=flat-square)](https://github.com/ggml-org/llama.cpp/pull/22897)

---

## About Me

I build production LLM systems from the metal up — from quantized models running on Jetson edge hardware to multi-agent cloud deployments with tool-use, permission gating, and audit trails. Currently focused on MoE fine-tuning, Blackwell-native FP4 quantization (NVFP4), and agentic coding benchmarks (SWE-bench).

*Open to ML Engineer roles — DFW or remote.*

---

## What I'm Building

### [Godspeed Coding Agent](https://github.com/t-timms/godspeed-coding-agent) [![CI](https://img.shields.io/github/actions/workflow/status/t-timms/godspeed-coding-agent/ci.yml?style=flat-square&label=CI)](https://github.com/t-timms/godspeed-coding-agent/actions/workflows/ci.yml)

Security-first open-source coding agent. Hand-rolled async ReAct loop with 4-tier deny-first permission engine, SHA-256 hash-chained audit trail, and 200+ LLM providers via LiteLLM. 4,600+ tests.

- **SWE-bench Lite (dev-23 split): 34.8% single-shot · 52.2% oracle best-of-5** — free-tier drivers, $0 API spend; [methodology](https://github.com/t-timms/godspeed-coding-agent#benchmarks)
- 30+ built-in tools with JSON Schema validation, MCP server + client
- Parallel + speculative tool dispatch, cost budget enforcement
- Self-evolution via LLM-guided mutations, multi-language verify gate with retry
- Training data export (openai/chatml/sharegpt), per-step reward annotations for GRPO

### [ZAYA1 NVFP4 W4A4 on Blackwell](https://github.com/t-timms/zaya1-godspeed)

End-to-end NVFP4 W4A4 quantization + serving for Zyphra's ZAYA1-8B (80-layer MoE + CCA attention) on a 16 GB RTX 5070 Ti. Rebuilt vLLM from source with SM120 CUTLASS FP4 kernels, wrote the layer-wise activation calibration, and reverse-engineered the NVFP4 global-scale convention.

- **9.5 tok/s single-stream · ~74 tok/s batch-8** (`enforce_eager=True`), 6.02 GB checkpoint
- **n-gram speculative decoding: validated 2.2× speedup** on coding-edit prompts, zero training required
- Budget-forced reasoning evals proving checkpoint health: GPQA-Diamond 45.8% → 62.5% with reasoning budget

### [Sovereign Edge](https://github.com/t-timms/sovereign-edge)

Autonomous multi-agent personal intelligence system on NVIDIA Jetson Orin Nano Super. 5 LangGraph expert agents, LiteLLM gateway (4 providers + Ollama), 3-tier ONNX intent router. 415 tests. Fully on-device — zero cloud dependencies.

### [Manna Trading](https://github.com/t-timms/manna-trading)

Multi-agent algorithmic trading pipeline with DeepSeek R1 reasoning at every stage. 4-agent pipeline (TA → Chief → Risk → Execution), Kelly Criterion position sizing, Monte Carlo risk simulation, real-time WebSocket market data.

### [Bible AI Assistant](https://github.com/t-timms/bible-ai-assistant)

Qwen3.5-4B fine-tuned with ORPO for biblical Q&A. Hybrid RAG (ChromaDB + BM25 + cross-encoder reranking), constitutional AI guardrails, voice pipeline (Whisper + Kokoro TTS), Gradio UI. 183 tests, 34 W&B runs, 5,925 training steps.

### More Projects

- **[GPU Server Test Suite](https://github.com/t-timms/gpu-server-test-suite)** — GPU fleet validation modeled on NVIDIA DCGM, Prometheus + Grafana dashboards. 188 tests.
- **[ML Lab](https://github.com/t-timms/ml-lab)** — Experiment lifecycle control plane, orchestrates gpu-server-test-suite and llm-wiki. 49 tests.
- **[LLM Wiki](https://github.com/t-timms/llm-wiki)** — Git-backed knowledge base, LangGraph ingest/query pipelines, BM25 search. 117 tests.
- **[ML Experiment Scaffold](https://github.com/t-timms/ml-experiment-scaffold)** — GitHub template for reproducible single-GPU ML experiments (config-driven, 3-seed reporting).
- **[Manufacturing Quality Analytics](https://github.com/t-timms/manufacturing-quality-analytics)** — SQL + Python ETL for semiconductor quality analysis.
- **[Tesla Tire Wear ML](https://github.com/t-timms/tesla-tire-wear-ml)** — Multi-model ensemble for tire wear prediction.

---

## Open Source Work

- **[llama.cpp #22897](https://github.com/ggml-org/llama.cpp/pull/22897)** — NVFP4 default type mapping + per-tensor scale tensors + MSE-optimal correction (open, awaiting upstream review)
- **[llama.cpp #22858](https://github.com/ggml-org/llama.cpp/pull/22858)** — Missing `LLAMA_FTYPE_MOSTLY_NVFP4` case fix (closed, replaced by #22897)

---

## GitHub Activity

<div align="center">
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
| **Inference** | vLLM (custom CUTLASS builds), llama.cpp, n-gram speculative decoding (2.2× validated) |
| **Quantization** | NVFP4 (Blackwell-native), GGUF, FP8, NF4, GPTQ, AWQ |
| **ML Infrastructure** | PyTorch, CUDA 12.8, torch.compile, DeepSpeed, lm-eval, W&B, MLflow |
| **Systems** | Python, TypeScript, Docker, GitHub Actions CI/CD, systemd |
| **Edge / Hardware** | NVIDIA Jetson Orin Nano Super, RTX 5070 Ti (Blackwell sm_120), 16 GB VRAM optimization |
| **Data** | PostgreSQL, SQL, pandas, SQLAlchemy, ChromaDB, LanceDB, BM25 |

---

<div align="center">

**Tremayne Timms** · [Portfolio](https://t-timms.github.io) · [GitHub](https://github.com/t-timms) · [LinkedIn](https://www.linkedin.com/in/tremayne-t-/) · [Email](mailto:ttimmsinternational@gmail.com)

</div>
