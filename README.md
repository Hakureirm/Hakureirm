<div align="center">

# Hakureirm

Inference stacks, on the wrong hardware.

<br>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Triton](https://img.shields.io/badge/Triton-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Verilog](https://img.shields.io/badge/Verilog-1A6FB4?style=flat-square&logo=v&logoColor=white)

<br>

> *The world opens itself before those with noble hearts.*

</div>

---

## What I actually do

I take inference stacks apart and put them back together somewhere they don't belong — a kernel that only compiles on SM120, a model that needs 1M context on cards without the right instructions, a 0.5B LLM on a RISC-V board with no NPU.

Most of it comes down to the same three things: **find where the abstraction assumed hardware it doesn't have, prove the replacement is numerically identical, then make it fast.** The proving part is where most of the time goes.

Background is embedded — Verilog, ESP32, RISC-V — which turns out to be exactly the right training for reading a kernel and asking *"but what does this actually do to the registers?"*

---

## Selected work

### 🚀 Inference where it shouldn't run

| | |
|---|---|
| **[rwkv-sglang](https://github.com/Hakureirm/rwkv-sglang)** | Production-grade RWKV-7 (Goose) inference for SGLang — exact correctness, int8, dynamic-batch serving, multi-GPU, FLA-free |
| **[rwkv-hf-kernels](https://github.com/Hakureirm/rwkv-hf-kernels)** | Optional fused CUDA kernels for the HuggingFace RWKV-7 model |
| **[rwkv7-hub](https://github.com/Hakureirm/rwkv7-hub)** | RWKV-7 for released `transformers` via Hub remote code — bit-identical checkpoint conversions, CPU/MPS/CUDA |
| **[minimax-m3-ampere](https://github.com/Hakureirm/minimax-m3-ampere)** | MiniMax-M3 with fp8 KV cache and full 1M context on Ampere (A100/A800, SM80) — patches plus the CUDA-graph gotcha that costs you a week |
| **[k230-llm](https://github.com/Hakureirm/k230-llm)** | A ~0.5B ternary LLM on a sub-$10 RISC-V edge board. CPU + RVV only. No NPU. |

### 🛠️ Tools for working with agents

| | |
|---|---|
| **[vibird](https://github.com/Hakureirm/vibird)** | Zero-config, cross-agent voice + status companion for vibe coding — talk to a desk device, watch your agent's live state, approve actions. Rust + ESP32. |
| **[feishu-agent-loop](https://github.com/Hakureirm/feishu-agent-loop)** | Supervise long-running agent tasks from Feishu/Lark — bot pushes progress, replies wake it in seconds |
| **[longport_mcp](https://github.com/Hakureirm/longport_mcp)** | MCP server for LongPort |

### 📐 Odds and ends

| | |
|---|---|
| **[tkkc-beamer](https://github.com/Hakureirm/tkkc-beamer)** | Unofficial LaTeX Beamer template for Xiamen University Tan Kah Kee College |
| **[USTC-Verilog-OJ-Solved](https://github.com/Hakureirm/USTC-Verilog-OJ-Solved)** | 中科大 Verilog OJ 个人题解 |
| **[ESP32-Arduino-DacaiCMD-Template](https://github.com/Hakureirm/ESP32-Arduino-DacaiCMD-Template)** | 移植到 ESP32 的大彩串口屏指令模板 |

---

## Currently

Getting DeepSeek-V4 to serve on SM80 — compile, dispatch, kernel, and an indexer intermediate that's several orders of magnitude too large. Upstream at [sgl-project/sglang](https://github.com/sgl-project/sglang).

---

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=Hakureirm&show_icons=true&include_all_commits=true&hide_border=true&theme=github_dark&icon_color=76B900&title_color=76B900">
  <img src="https://github-readme-stats.vercel.app/api?username=Hakureirm&show_icons=true&include_all_commits=true&hide_border=true&theme=graywhite&icon_color=76B900&title_color=2F81F7" alt="stats" height="165">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Hakureirm&layout=compact&hide=html,tex&count_private=true&hide_border=true&theme=github_dark&title_color=76B900">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Hakureirm&layout=compact&hide=html,tex&count_private=true&hide_border=true&theme=graywhite&title_color=2F81F7" alt="languages" height="165">
</picture>

<br><br>

![visitors](https://visitor-badge.laobi.icu/badge?page_id=Hakureirm.readme&title=visitors&title_bg=%23555555&color=%2376B900)

<sub>Still, nominally, a corporate slave. ⚡</sub>

</div>
