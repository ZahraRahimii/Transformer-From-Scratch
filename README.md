# Transformer-From-Scratch
This project implements a Transformer model from scratch using PyTorch, for English-to-German translation.

## Project Overview

1. **Attention Module**

   * Implement Scaled Dot-Product Self-Attention.
   * Extend to Multi-Head Attention by splitting and combining heads.

2. **Feed Forward Network**

   * Two-layer neural network with ReLU activation.
   * Includes Layer Normalization and residual connections.

3. **Encoder**

   * A stackable encoder block with:

     * Multi-Head Self-Attention
     * Feed Forward
     * Add & Norm

4. **Decoder**

   * Decoder block containing:

     * Masked Multi-Head Self-Attention
     * Encoder–Decoder Attention
     * Feed Forward + Add & Norm
   * Includes future-masking for self-attention.

5. **Positional Encoding & Embedding**

   * Implement word embeddings using `torch.nn.Embedding`.
   * Add sinusoidal positional encodings to input sequences.

6. **Transformer Architecture**

   * Combine encoder and decoder into a unified model class.
   * Accept hyperparameters like `d`, `h`, `Ne`, `Nd`, `dff`, `L`.

7. **Training**

   * Use short English-German sentence pairs.
   * Tokenize, pad, and prepare inputs.
   * Train with Cross-Entropy Loss and `Adam` optimizer.

