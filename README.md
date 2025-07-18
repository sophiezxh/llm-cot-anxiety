# llm-cot-anxiety
Causal Analysis of Chain-of-Thought Reasoning in LLM-Based Anxiety Detection, part of University of Iowa SSTP 2025 and in collaboration with University of Iowa's Department of Business Analytics

# Interpretable LLM Reasoning for Mental Health Text Classification

This repository contains code, results, and analysis for a summer research project exploring the interpretability of large language models (LLMs) in the context of mental health, specifically focusing on anxiety detection from Reddit posts.

## 📌 Project Overview

We investigate how reasoning types and step positions in Chain-of-Thought (CoT) explanations affect the final predictions made by LLMs. Using a dataset of 8,000 Reddit posts from r/anxiety, we analyze which steps are most causally responsible for model predictions and test stability through ablation and counterfactual perturbations.

## 🔍 Key Findings

- **Later reasoning steps** are more influential in model predictions.
- The model is **robust to step removal** but **sensitive to replacement**, indicating selective reliance on specific reasoning.
- **Emotion- and worry-related reasoning types** are the most causally influential.
- Reasoning related to **symptoms and treatments** contributes the least to model output.

## 🛠️ Methodology

- **Model**: DeepSeek-v2 using Chain-of-Thought prompting
- **Dataset**: 8,000 annotated Reddit posts from r/anxiety (private; **not publicly shareable** due to privacy concerns)
- **Analyses**: Flip-rate metrics, ablation tests, counterfactual replacements, and causal reasoning classification

## 📁 Files

- `notebook.ipynb` — Jupyter Notebook with full analysis pipeline
- `ablation_results.csv` — Results from step deletion tests
- `counterfactual_results.csv` — Replacement test outcomes
- `reasoning_step_labels.csv` — Manual reasoning type labels

## 🔮 Future Directions

- Improve reasoning quality for underperforming types (e.g., symptom-related).
- Explore multi-modal input for deeper interpretability (e.g., speech, video).
- Build clinical-aligned LLMs that prioritize emotional sensitivity and stability.

## 🔒 Dataset Privacy Notice

The dataset used in this project is private and **cannot be publicly shared** due to ethical considerations and user privacy concerns. Please contact the project author for questions regarding data access for academic collaboration only.

## 📄 License

This project is for academic and research purposes only.
