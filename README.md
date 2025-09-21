# Ranking Fairness in AI Hiring
### A Benchmark of LLMs, Embeddings, and Classical Methods
---

This repository contains experiments investigating **bias in candidate reranking using Large Language Models (LLMs)**. The study evaluates how LLMs, embeddings, and classical methods behave when ranking resumes against a fixed job description, with a focus on **fairness, consistency, and bias mitigation**.

## Overview

This project benchmarks multiple model categories on **resume ranking fairness** in AI-driven hiring:  
- **Proprietary LLMs** (GPT-4, Claude, Gemini, etc.)  
- **Open-Source LLMs** (Mistral, LLaMA, Phi-3)  
- **Embedding Models** (MiniLM, MPNet, GTE, E5)  
- **Classical Baselines** (BM25, TF-IDF)  

Experiments test for:  
- **Name Bias**  
- **Order Bias**  
- **Consistency**  
- **Anomalies**  
- **Bias Mitigation Strategies**

## Repository Structure

- **`notebooks/`**  
  Contains Jupyter notebooks used for running experiments.  
  - `llm_reranking_bias.ipynb`: Initial notebook (without NDCG evaluation).  
  - `llm_reranking_bias_with_ndcg_score.ipynb`: Updated notebook including NDCG@20 scoring.  

- **`html_notebooks/`**  
  HTML exports of the notebooks for easy viewing.  
  - `llm_reranking_bias.html`  
  - `llm_reranking_bias_with_ndcg_score.html`  

- **`results/`**  
  Contains evaluation outputs for all experiments, stored in PDF format.  
  - `classical_methods_results/`: Results for BM25 and TF-IDF.  
  - `embedding_models_results/`: Results for MiniLM, MPNet, GTE, E5, etc.  
  - `opensource_llm_results/`: Results for open-source LLMs (Mistral, LLaMA, Phi, etc.).  

## How to Use

1. Open the `.ipynb` notebooks in **Jupyter Notebook** or **VS Code** to rerun experiments.
2. Use the `.html` exports for quick browsing without needing a Python environment.
3. Refer to the **with\_ndcg\_score** notebooks for the most complete results, including ranking metrics.

## Notes

* Proprietary LLM outputs (e.g., GPT, Claude, Gemini) are **not included** due to licensing restrictions.
* Open-source models and classical baselines are fully reproducible with the provided code.
* Neutral naming and token replacement experiments are included to demonstrate bias mitigation.
* This repository complements the associated research paper, where results, heatmaps, and discussion are presented.
