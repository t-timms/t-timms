<div align="center">

# Tremayne Timms

**ML Engineer** — LLM quantization & inference on consumer hardware

Dallas–Fort Worth, TX · [Portfolio](https://t-timms.github.io) · [Hugging Face](https://huggingface.co/Ttimms) · [LinkedIn](https://www.linkedin.com/in/tremayne-t-/) · [ttimmsinternational@gmail.com](mailto:ttimmsinternational@gmail.com)

<picture>
  <source srcset="https://skillicons.dev/icons?i=python%2Cpytorch%2Ccpp%2Cdocker%2Cgithubactions%2Clinux&theme=dark" media="(prefers-color-scheme: dark)" />
  <img src="https://skillicons.dev/icons?i=python%2Cpytorch%2Ccpp%2Cdocker%2Cgithubactions%2Clinux" alt="Python, PyTorch, C++, Docker, GitHub Actions, Linux" />
</picture>

</div>

---

I quantize and serve large models on hardware that isn't supposed to run them — 16 GB Blackwell GPUs, Jetson edge boards — and I reproduce every published number against its confidence interval before I call it done.

**15 models on Hugging Face · ~7,800 downloads/month** *(Sept 2026)*.

*Open to ML Engineer roles (inference optimization, model compression, edge deployment) — DFW or remote.*

## Projects

**[Bible AI Assistant](https://github.com/t-timms/bible-ai-assistant)** — Local Scripture Q&A on a 16 GB card: hybrid RAG over 31k verses feeding an SFT fine-tune, with a verifiable-citation reward (cited verse must exist in the index, quote must match) scaffolded for a GRPO stage. sha256-pinned benchmark protocol, 476 tests, full CI/CD. Primary project — building toward local SOTA on a 5070 Ti.

**[MoE Pruning + NVFP4](https://github.com/t-timms/kat-coder-nvfp4)** — A 50%-expert-pruned MoE coder model, quantized to fit 16 GB VRAM. SWE-bench Verified 52.0% (26/50, officially graded), HumanEval+/MBPP+ reproduced inside published confidence intervals, CI-checked reproduction pipeline. [Model on Hugging Face →](https://huggingface.co/Ttimms/KAT-Coder-V2.5-Dev-REAP-50-NVFP4A16)

**[Ornith REAP-50 + NVFP4](https://github.com/t-timms/ornith-nvfp4)** — Same pipeline on a different 35B-A3B MoE base (MIT): 256→128 experts, MTP head and vision tower stripped, GPTQ-NVFP4A16 — 12.47 GiB. SWE-bench Verified 44.0% (22/50, official harness, same 50-instance slice as the KAT run), HumanEval+ 84.2% / MBPP+ 89.2%. Three upstream vLLM gaps for this architecture patched locally. [Model on Hugging Face →](https://huggingface.co/Ttimms/Ornith-1.5-35B-A3B-REAP-50-NVFP4A16)

**[ZAYA1 NVFP4 W4A4](https://github.com/t-timms/zaya1-nvfp4-w4a4)** — 4-bit weights *and* activations on native Blackwell tensor cores: 9.5 tok/s single-stream from a 6.02 GB checkpoint, 2,400+ combined downloads on Hugging Face (Sept 2026). Includes a benchmark I retracted and corrected in public once I found the CUDA-graph path corrupting output. [Model on Hugging Face →](https://huggingface.co/Ttimms/zaya1-8b-nvfp4-w4a4)

**[Godspeed Coding Agent](https://github.com/t-timms/godspeed-coding-agent)** — A coding agent built from scratch: deny-first permission engine, SHA-256 hash-chained audit trail. SWE-bench Lite 34.8% single-shot / 52.2% oracle best-of-5, $0 API spend.

**[Sovereign Edge](https://github.com/t-timms/sovereign-edge)** — Five-agent personal AI system running entirely on a Jetson Orin Nano — zero cloud dependencies.

Also: [Manna Trading](https://github.com/t-timms/manna-trading) (multi-agent trading pipeline) · an [open llama.cpp PR](https://github.com/ggml-org/llama.cpp/pull/22897) fixing an NVFP4 quantizer crash

## Stack

Python · PyTorch · vLLM / CUTLASS · TRL / Unsloth · NVFP4 · GGUF · GPTQ / AWQ · CUDA · Docker

---

<div align="center">

[Portfolio](https://t-timms.github.io) · [Hugging Face](https://huggingface.co/Ttimms) · [LinkedIn](https://www.linkedin.com/in/tremayne-t-/) · [ttimmsinternational@gmail.com](mailto:ttimmsinternational@gmail.com)

</div>
