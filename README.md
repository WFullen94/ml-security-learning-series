# ML Security Learning Series

A self-directed curriculum covering the full ML and AI security stack — from inference systems and representation learning through adversarial ML, LLM security, reinforcement learning, and probabilistic reasoning.

Each series is self-contained with runnable notebooks. Methods that are historically important but no longer used in production are covered in narrative markdown. Code is reserved for techniques that are production- or research-relevant today.

---

## Curriculum

| # | Series | Notebooks | Topics |
|---|--------|-----------|--------|
| 1 | [LLM Systems & Inference](./01-llm-systems-and-inference/) | 20 | Tokenization, transformers, KV cache, quantization, vLLM, speculative decoding |
| 2 | [Representation Learning](./02-representation-learning/) | 20 | Word2Vec→CLIP, contrastive learning, FAISS, RAG, embedding drift |
| 3 | [ML Security](./03-ml-security/) | 20 | Adversarial examples, membership inference, backdoors, supply chain, DP-SGD |
| 4 | [LLM Security](./04-llm-security/) | 17 | Prompt injection, jailbreaks, RAG poisoning, canary tokens, red teaming |
| 5 | [Reinforcement Learning](./05-reinforcement-learning/) | 15 | DQN, PPO, SAC, safe RL, RLHF, policy explanation |
| 6 | [Bayesian Inference](./06-bayesian-inference/) | 15 | PyMC, HMC/NUTS, hierarchical models, GPs, Bayesian A/B testing |
| 7 | [Statistical ML Evaluation](./07-statistical-ml-evaluation/) | 17 | Bootstrap CI, calibration, subgroup analysis, drift detection, conformal prediction |
| 8 | [Causal Inference](./08-causal-inference/) | 12 | DAGs, propensity scoring, DiD, RDD, double ML, causal forests |
| 9 | [Anomaly Detection](./09-anomaly-detection/) | 11 | Isolation Forest, autoencoders, VAEs, LSTM, PatchCore, streaming detection |
| 10 | [Graph ML & GNNs](./10-graph-ml/) | 12 | GCN, GraphSAGE, GAT, GIN, knowledge graphs, graph transformers, AST vulnerability detection |

---

## Setup

```bash
# Clone
git clone https://github.com/wfullen/ml-security-learning-series
cd ml-security-learning-series

# Install nbstripout (keeps notebook outputs out of git)
pip install nbstripout
nbstripout --install

# Each series has its own dependencies — install as needed
pip install torch torchvision numpy pandas scikit-learn matplotlib
```

---

## Conventions

- **Narrative markdown** — historical or superseded methods are explained in prose. No code for algorithms that are no longer used in practice.
- **Code** — reserved for methods that are production- or research-relevant today.
- **Capstone notebooks** — each series ends with an end-to-end pipeline tying all concepts together, often as a prototype of a tool from the project backlog.

---

## Related Projects

These notebooks serve as the foundation and prototyping ground for standalone tools:

| Tool | Prototype in |
|------|-------------|
| `benchpress` | Series 1, NB 20 |
| `bouncer` | Series 4, NB 14 |
| `memory-leak` | Series 3, NB 04 |
| `gymcheck` | Series 5, NB 10 |
| `shaky` | Series 7, NB 10 |
| `honest-abe` | Series 7, NB 06 |
| `drift-cam` | Series 9, NB 11 |
| `oracle` | Series 6, NB 15 |
| `semantic-vuln-chain-analysis` | Series 10, NB 12 |
