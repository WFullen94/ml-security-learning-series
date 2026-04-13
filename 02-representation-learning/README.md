# Series 2 · Representation Learning

Covers the full arc of learned representations — from static word vectors through contrastive self-supervised learning, multimodal embeddings, and production retrieval systems. Builds toward `drift-cam` (semantic drift monitor) and `label-noise` (mislabelled image detector).

**Narrative only** (no code): Word2Vec, GloVe, ELMo — objectives and why they lost to contextual models.

## Notebooks

| # | Notebook | Topics |
|---|----------|--------|
| 01 | Static Embeddings | Word2Vec/GloVe narrative; FastText for OOV and multilingual |
| 02 | Contextual Embeddings | ELMo→BERT narrative; sentence-transformers, semantic search |
| 03 | Fine-Tuning Embeddings | Domain contrastive fine-tuning with sentence-transformers |
| 04 | Contrastive Learning | SimCLR from scratch — NT-Xent loss, augmentation, projection head |
| 05 | Momentum Contrast (MoCo) | Memory queue + momentum encoder |
| 06 | Self-Supervised Vision: DINO | Self-distillation, emergent segmentation |
| 07 | Multimodal Embeddings: CLIP | Zero-shot classification and image-text retrieval |
| 08 | Probing Classifiers | Linear probing on frozen CLIP/DINO features |
| 09 | Embedding Evaluation | STS, recall@k, MTEB; benchmark pitfalls |
| 10 | Dimensionality Reduction | PCA vs UMAP vs t-SNE; interactive visualisation |
| 11 | Approximate Nearest Neighbours | FAISS — HNSW, IVF, product quantization |
| 12 | Vector Databases | pgvector vs dedicated DBs; architecture tradeoffs |
| 13 | Retrieval-Augmented Generation | End-to-end RAG with sentence-transformers + retrieval eval |
| 14 | Embedding Drift Detection | Statistical drift tests on embedding streams — `drift-cam` foundation |
| 15 | Cross-Modal Retrieval | CLIP-based image↔text search pipeline |
| 16 | Model Fingerprinting via Embeddings | Embedding distribution analysis — `whodunit` foundation |
| 17 | Label Noise Detection | CLIP/DINOv2 + clustering for mislabelled samples — `label-noise` foundation |
| 18 | Tabular Representations | Entity embeddings, TabNet |
| 19 | Self-Supervised Tabular & Time Series | SCARF, TS2Vec contrastive pretraining |
| 20 | Capstone: Semantic Drift Monitor | `drift-cam` prototype — CLIP embeddings + streaming drift detection |

## Dependencies

```bash
pip install torch torchvision sentence-transformers faiss-cpu numpy matplotlib umap-learn
```
