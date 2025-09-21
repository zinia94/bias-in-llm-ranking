# Ranking Fairness in AI Hiring
### A Benchmark of LLMs, Embeddings, and Classical Methods
---

This repository contains experiments investigating **bias in candidate reranking using Large Language Models (LLMs)**. The study evaluates how LLMs, embeddings, and classical methods behave when ranking resumes against a fixed job description, with a focus on **fairness, consistency, and bias mitigation**.

The experiments specifically examine:

* **Name bias** – whether candidate names affect rankings despite identical content.
* **Order bias** – whether the sequence of resumes influences results.
* **Consistency checks** – whether repeated runs with the same input yield stable outputs.
* **Bias mitigation** – whether anonymization (neutral labels, token replacement) reduces bias.

## Repository Contents

* **notebooks/llm\_reranking\_bias.ipynb**
  Initial Jupyter Notebook implementation of the bias evaluation framework. Includes:

  * Resume templates (strong vs. weak profiles).
  * Candidate name variations.
  * Baseline experiments across LLMs, embeddings, and classical models.

* **notebooks/llm\_reranking\_bias\_with\_ndcg\_score.ipynb**
  Extended version of the notebook with additional **NDCG\@20 (Normalized Discounted Cumulative Gain)** evaluation.

* **html_notebooks/llm\_reranking\_bias.html**
  Exported HTML version of the initial notebook (viewable in any browser without Jupyter).

* **html_notebooks/llm\_reranking\_bias\_with\_ndcg\_score.html**
  Exported HTML version of the extended notebook.


## How to Use

1. Open the `.ipynb` notebooks in **Jupyter Notebook** or **VS Code** to rerun experiments.
2. Use the `.html` exports for quick browsing without needing a Python environment.
3. Refer to the **with\_ndcg\_score** notebooks for the most complete results, including ranking metrics.


## Notes

* Proprietary LLM outputs (e.g., GPT, Claude, Gemini) are **not included** due to licensing restrictions.
* Open-source models and classical baselines are fully reproducible with the provided code.
* Neutral naming and token replacement experiments are included to demonstrate bias mitigation.
* This repository complements the associated research paper, where results, heatmaps, and discussion are presented.
