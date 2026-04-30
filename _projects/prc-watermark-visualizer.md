---
title: "PRC Watermark Visualizer"
date: 2026-04-30
description: "Interactive visualizer for exploring pseudorandom code watermarks in LLM outputs."
tags: ["watermarking", "cryptography", "llm", "visualization"]
demo: "/visualizers/prc/"
---

A pseudorandom code (PRC) watermark hides a codeword inside the bits of a sampled response. Detection is a soft majority vote over a sparse parity-check matrix `P`: count how many parity checks of `Px ⊕ Pz` are unsatisfied, and output 1 if that count falls below `(½ − ζ)·r`. 

The catch is that not every token position carries signal — when the language model is essentially deterministic at a position, the watermark can't reliably embed anything there, and parity checks dominated by such positions are wasted: they add variance to the count without contributing information.

## Interactive Features

1. **Click any token** in the response to see exactly which parity checks constrain that bit position
2. **Hover a parity check** to see which tokens it touches, lit up in the response above
3. The decoder opens by **rejecting** (`output ⊥`). Click the *prune low-quality* button — it removes the parity checks whose support is ≥ 60% low-entropy positions. The verdict flips to *output 1* (watermark detected)

## Data

Built from a real run of Qwen3-0.6B with 60 sampled tokens and empirical entropies `H = −log₂ p(token)` recorded at each step.

## Insight

The pedagogical claim this lands: a parity check whose support is dominated by language-model-deterministic positions can't actually distinguish watermarked text from pad-only noise — it just adds variance to the unsat count. Filtering these out is morally what the empirical-entropy weighting in §7 of the Christ–Gunn paper is doing in continuous form.

<iframe
  src="/visualizers/prc/"
  width="100%"
  height="980"
  loading="lazy"
  style="border: 1px solid #2a2b30; border-radius: 4px; background: #0c0d10;"
  title="LDPC-PRC Watermark Inspector">
</iframe>
