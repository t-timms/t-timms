<div align="center">

# Tremayne Timms

**ML Engineer** — LLM quantization & inference on consumer hardware

Dallas–Fort Worth, TX · [Portfolio](https://t-timms.github.io) · [Hugging Face](https://huggingface.co/Ttimms) · [LinkedIn](https://www.linkedin.com/in/tremayne-t-/) · [ttimmsinternational@gmail.com](mailto:ttimmsinternational@gmail.com)

<picture>
  <source srcset="https://skillicons.dev/icons?i=python%2Cpytorch%2Cdocker%2Cgithubactions%2Cts%2Cpostgres&theme=dark" media="(prefers-color-scheme: dark)" />
  <img src="https://skillicons.dev/icons?i=python%2Cpytorch%2Cdocker%2Cgithubactions%2Cts%2Cpostgres" alt="Python, PyTorch, Docker, GitHub Actions, TypeScript, PostgreSQL" />
</picture>

</div>

---

I quantize and serve large models on hardware that isn't supposed to run them — 16 GB Blackwell GPUs, Jetson edge boards — and I reproduce every published number against its confidence interval before I call it done.

*Open to ML Engineer roles — DFW or remote.*

## Projects

**[Bible AI Assistant](https://github.com/t-timms/bible-ai-assistant)** — Local Scripture Q&A on a 16 GB card: hybrid RAG over 31k verses feeding an SFT → ORPO → GRPO fine-tune with a *verifiable* reward — the cited verse must exist in the index and the quote must match. sha256-pinned benchmark protocol, 430 tests, full CI/CD. Primary project — building toward local SOTA on a 5070 Ti.

**[MoE Pruning + NVFP4](https://github.com/t-timms/kat-coder-nvfp4)** — A 50%-expert-pruned MoE coder model, quantized to fit 16 GB VRAM. SWE-bench Verified 52.0% (26/50, officially graded), HumanEval+/MBPP+ reproduced inside published confidence intervals, CI-checked reproduction pipeline. [Model on Hugging Face →](https://huggingface.co/Ttimms/KAT-Coder-V2.5-Dev-REAP-50-NVFP4A16)

**[ZAYA1 NVFP4 W4A4](https://github.com/t-timms/zaya1-nvfp4-w4a4)** — 4-bit weights *and* activations on native Blackwell tensor cores: 9.5 tok/s single-stream from a 6.02 GB checkpoint, 2,100+ combined downloads on Hugging Face. Includes a benchmark I retracted and corrected in public once I found the CUDA-graph path corrupting output. [Model on Hugging Face →](https://huggingface.co/Ttimms/zaya1-8b-nvfp4-w4a4)

**[Godspeed Coding Agent](https://github.com/t-timms/godspeed-coding-agent)** — A coding agent built from scratch: deny-first permission engine, SHA-256 hash-chained audit trail. SWE-bench Lite 34.8% single-shot / 52.2% oracle best-of-5, $0 API spend.

**[Sovereign Edge](https://github.com/t-timms/sovereign-edge)** — Five-agent personal AI system running entirely on a Jetson Orin Nano — zero cloud dependencies.

Also: [Manna Trading](https://github.com/t-timms/manna-trading) (multi-agent trading pipeline) · an [open llama.cpp PR](https://github.com/ggml-org/llama.cpp/pull/22897) fixing an NVFP4 quantizer crash

## Stack

Python · PyTorch · vLLM / CUTLASS · TRL / Unsloth · NVFP4 · GGUF · GPTQ / AWQ · CUDA · Docker

---

<div align="center">

[Portfolio](https://t-timms.github.io) · [Hugging Face](https://huggingface.co/Ttimms) · [LinkedIn](https://www.linkedin.com/in/tremayne-t-/) · [ttimmsinternational@gmail.com](mailto:ttimmsinternational@gmail.com)

</div>
