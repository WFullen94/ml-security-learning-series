# Series 1 · LLM Systems & Inference

Covers the internals of large language model inference — from tokenization through serving infrastructure. Builds toward a benchmarking pipeline (`benchpress`) for speed + quality evaluation on Apple Silicon.

**Narrative only** (no code): early positional encodings (sinusoidal, learned fixed), vanilla multi-head attention derivation, static batching.

## Notebooks

| # | Notebook | Topics |
|---|----------|--------|
| 01 | Tokenization & Vocabularies | BPE, WordPiece, SentencePiece, vocabulary size tradeoffs |
| 02 | Transformer Architecture | Attention, MLP, LayerNorm, residual stream — from scratch |
| 03 | Sampling Strategies | Temperature, top-k, top-p, nucleus sampling |
| 04 | Decoding Algorithms | Greedy vs beam search vs stochastic; tradeoffs |
| 05 | KV Cache | What it stores, why it matters, memory math |
| 06 | Flash Attention | Memory-efficient attention internals |
| 07 | PagedAttention | vLLM's core innovation; KV cache fragmentation |
| 08 | Prefix & Prompt Caching | Reusing KV cache across requests |
| 09 | Quantization | INT8, INT4, GGUF — quality vs compression |
| 10 | Speculative Decoding | Draft models, acceptance rates |
| 11 | Continuous Batching | Dynamic request streams vs static batching |
| 12 | Serving Metrics | TTFT, TBT, throughput, latency/throughput tradeoff |
| 13 | Running Local Models | llama.cpp, ollama, MLX on Apple Silicon |
| 14 | vLLM Internals | Architecture walkthrough |
| 15 | Structured Decoding | JSON mode, constrained generation |
| 16 | Positional Encoding & RoPE | How models handle position; long context |
| 17 | Context Length Extension | YaRN, RoPE scaling |
| 18 | Parallelism Strategies | Tensor/pipeline parallelism concepts |
| 19 | LLM Routing & Cost Optimization | Quality-adaptive routing; `dispatch` foundation |
| 20 | Capstone: Benchmarking Pipeline | `benchpress` prototype — speed + quality + stats |

## Dependencies

```bash
pip install torch transformers tokenizers numpy matplotlib
```
