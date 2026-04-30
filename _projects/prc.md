---
title: "PRC Watermark Visualizer"
date: 2026-01-01
description: "Interactive visualizer for exploring pseudorandom code watermarks in LLM outputs."
tags: ["watermarking"]
github: "https://github.com/anuragkashyap"
demo: "/visualizers/prc/"
permalink: /projects/prc-visualizer/
---

A pseudorandom code (PRC) watermark hides a codeword inside the bits of a sampled response. Detection uses a soft majority vote over a sparse parity-check matrix.

The interactive visualizer explores how entropy-weighted parity checks improve watermark detection by filtering out low-quality checks dominated by high-entropy positions.

Visit the [interactive visualizer](/visualizers/prc/) to explore the watermark detection process.
