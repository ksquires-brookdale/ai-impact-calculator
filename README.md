# AI Tokenization & Impact Calculator

This repository hosts the **AI Tokenization & Impact Calculator**, an interactive single-page web tool built for general education *Introduction to AI* coursework. It allows students to visualize how large language models break text into tokens and estimate the financial, electricity, and water footprint of AI usage at scale.

## Live Student Link

Hosted via GitHub Pages: https://ksquires-brookdale.github.io/ai-impact-calculator/

## Features

* **Interactive BPE Tokenization:** Splits prompts and AI responses into real tokens with color-coded chips and an optional toggle to view numeric Token IDs.
* **Starter Prompts:** Includes 40 built-in general-interest prompts with one-click random loading and copy-to-clipboard support.
* **Configurable Pricing & Model Tiers:** Editable API pricing (per 1M input/output tokens) and three energy/water estimation tiers (*Small / Fast*, *Standard Frontier*, and *Heavy Reasoning*).
* **4-Tier Impact Ladder:** Scales cost, electricity, and water usage—alongside everyday equivalents—across four levels:
  1. **Just You** (1 student × prompts per student)
  2. **Your Class** (class size × prompts per student)
  3. **Every U.S. College** (~3,800 degree-granting institutions via NCES IPEDS)
  4. **Worldwide** (single execution across ~1.2 billion global AI users)
* **Assignment Export:** Validates required fields and generates a formatted, multi-page PDF report (with a browser Print fallback) for LMS submission.

## Project Files

This repository contains both the readable source file and the live production file hosted by GitHub Pages:

* **`comp119-token-impact.html`** — The readable development/source file.
* **`index.html`** — The live production file served by GitHub Pages (with obfuscated JavaScript).
  
## External Dependencies

No build step or local package installation is required. The page loads two ES modules directly via `esm.sh`:

* `gpt-tokenizer` (MIT License) — Client-side BPE tokenization (`encode` / `decode`)
* `jspdf` (MIT License) — Client-side PDF generation

## Estimation Baselines

* **U.S. Higher Education:** 3,800 degree-granting colleges and universities (NCES IPEDS).
* **Global AI Users:** ~1.2 billion users (conservative standalone AI app user estimate), modeled as a single execution of the submitted prompt.
* **Energy & Water:** Educational estimates derived from published per-token inference benchmarks, scaled automatically across units (`Wh`–`GWh`, `mL`–`L`).

## License & Attribution

**Copyright © 2026 Kevin Squires**

This work is licensed under a [Creative Commons Attribution–NonCommercial 4.0 International License (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/). You are free to share and adapt this material for non-commercial purposes, provided you give appropriate credit, provide a link to the license, and indicate if changes were made.

**AI Assistance:** Engineered with coding and layout assistance from Google Gemini.
