# LLM Reranking Bias

This repository contains experiments investigating **bias in candidate reranking using Large Language Models (LLMs)**. The study evaluates how LLMs, embeddings, and classical methods behave when ranking resumes against a fixed job description, with a focus on **fairness, consistency, and bias mitigation**.

The experiments specifically examine:

* **Name bias** – whether candidate names affect rankings despite identical content.
* **Order bias** – whether the sequence of resumes influences results.
* **Consistency checks** – whether repeated runs with the same input yield stable outputs.
* **Bias mitigation** – whether anonymization (neutral labels, token replacement) reduces bias.

## Repository Contents

* **llm\_reranking\_bias.ipynb**
  Initial Jupyter Notebook implementation of the bias evaluation framework. Includes:

  * Resume templates (strong vs. weak profiles).
  * Candidate name variations.
  * Baseline experiments across LLMs, embeddings, and classical models.

* **llm\_reranking\_bias.html**
  Exported HTML version of the initial notebook (viewable in any browser without Jupyter).

* **llm\_reranking\_bias\_with\_ndcg\_score.ipynb**
  Extended version of the notebook with additional **NDCG\@20 (Normalized Discounted Cumulative Gain)** evaluation.

  * Provides a **quantitative metric** for ranking quality.
  * Captures subtle differences between models under bias experiments.
  * Complements qualitative analysis with reproducible numbers.

* **llm\_reranking\_bias\_with\_ndcg\_score.html**
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

Would you like me to also add a **"Structure of Experiments" section** (like listing the bias types and CV templates setup) so the README itself serves as a mini-summary of your paper?
