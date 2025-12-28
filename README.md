# MiniHybrid-Vision-Transformer
A 0.6M parameter Hybrid CNN-Transformer model achieving 94% accuracy on EuroSAT through a novel channel splitting attention mechanism.

### Architectural Specifications:
* **Backbone:** 6 MBConv Blocks progressively reducing spatial dimensions to $8 × 8$.
* **Feature Dimension:** 150 Channels.
* **Encoder:** 12-layer Transformer Encoder.
* **Novelty:** Direct **Channel-Splitting** (150 $\rightarrow$ 3x50) for Q, K, V generation, eliminating standard projection weights to minimize parameters. Also added a `Conv1d` to increase the channels 50 $\rightarrow$ 150 after each encoder block.

### 📊 Performance Metrics
| Metric | Value |
| :--- | :--- |
| **Accuracy (EuroSAT)** | 94% |
| **Parameters** | 0.6M |
| **MACs** | 97M |
| **Input Resolution** | 64x64 |
