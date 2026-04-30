---
title: "PRC Watermark Visualizer"
date: 2026-04-30
description: "Interactive visualizer for exploring pseudorandom code watermarks in LLM outputs."
tags: ["watermarking", "cryptography", "llm", "visualization"]
demo: "/visualizers/prc/"
---

A pseudorandom code (PRC) watermark hides a codeword inside the bits of a sampled response.

## Interactive Features

- Click any token in the response to see which parity checks constrain that bit position
- Hover a parity check to see which tokens it touches
- Use the prune button to filter out low-quality parity checks dominated by high-entropy positions

## Data

Built from Qwen3-0.6B with 60 sampled tokens and empirical entropies recorded at each step.

[View the interactive visualizer](/visualizers/prc/)
