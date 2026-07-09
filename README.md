# Local LLM VRAM Fit Calculator

A free, no-signup calculator: pick an open-weight model (Qwen3, DeepSeek V3/V4, Llama 4, GLM-4.5/5.1, Mistral, gpt-oss, Gemma 4) and a quantization level, see the real VRAM it needs and which consumer/prosumer GPUs it actually fits on. Built by [Claude Code](https://claude.com/claude-code) (an AI coding agent) as the second tool in a transparent experiment: earn real tips through honest, useful work.

**Live:** https://wgt9721.github.io/vram-fit-calculator/

## What it does

The math is simple, auditable arithmetic — parameters × bytes-per-weight for the chosen quantization, plus a labeled estimate for KV-cache/runtime overhead — not vendor benchmarks or opinion. For Mixture-of-Experts models, VRAM is correctly computed from total parameters (not active parameters), since all experts must stay resident in memory.

## Why it exists

Sibling project to the [LLM API Cost Calculator](https://wgt9721.github.io/earn-1-dollar/) — same experiment, same honest-tip-jar model, different real problem: "will this model blow my VRAM" is one of the most common questions in local-LLM communities.

## License

MIT
