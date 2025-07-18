# llm-cot-anxiety
Causal Analysis of Chain-of-Thought Reasoning in LLM-Based Anxiety Detection, part of University of Iowa SSTP 2025 and in collaboration with University of Iowa's Department of Business Analytics. 

# Interpretable LLM Reasoning for Mental Health Text Classification

This repository contains code, results, and analysis for the SSTP research project exploring the interpretability of large language models (LLMs) in the context of mental health, specifically focusing on anxiety detection from Reddit posts.

## 📌 Project Overview

We investigate how reasoning types and step positions in Chain-of-Thought (CoT) explanations affect the final predictions made by LLMs. Using a dataset of 5,000 Reddit posts from r/anxiety, we analyze which steps are most causally responsible for model predictions and test stability through ablation and counterfactual perturbations.

## 🔍 Key Findings

- **Later reasoning steps** are more influential in model predictions.
- The model is **robust to step removal** but **sensitive to replacement**, indicating selective reliance on specific reasoning.
- **Emotion- and worry-related reasoning types** are the most causally influential.
- Reasoning related to **symptoms and treatments** contributes the least to model output.
- **Reasoning is distributed across multiple types**, with no single type universally dominating.
- **Flip behavior reveals model fragility**, especially when reasoning steps are contradicted.

## 🛠️ Methodology

This study uses a structured intervention-based design to evaluate the causal role of reasoning steps in LLM predictions. A total of 5,000 Reddit posts from the r/anxiety subreddit were first labeled for anxiety manually. DeepSeek-V3 was then prompted to generate CoT reasoning and anxiety predictions for each post, which served as the baseline outputs.

Each CoT was segmented and classified by reasoning type:  
- Emotion  
- Symptom  
- Daily life  
- Treatment  
- Worry  
- Vague

Two forms of intervention were applied to each reasoning step:
1. **Ablation**: removing the reasoning step entirely.
2. **Counterfactual ablation**: replacing the step with its opposite meaning.

The study then computed flip rates across reasoning types and step positions to identify where and how prediction changes occurred. Additional baseline metrics (e.g., accuracy, F1) and the helpful flip rate were calculated to assess model performance. Final analysis focused on how these perturbations impacted interpretability and the causal attribution of reasoning in model predictions.

## 📁 Files

- `notebook.ipynb` — Jupyter Notebook with full analysis pipeline
- `ablation_results.csv` — Results from step deletion tests
- `counterfactual_results.csv` — Replacement test outcomes
- `reasoning_step_labels.csv` — Manual reasoning type labels

## 🔮 Future Directions

- Causal finetuning by reasoning type
- Counterfactual robustness training
- Human-in-the-loop interpretability tools
- Explore distributed reasoning and hybrid attribution methods
- Improve model robustness to contradictory reasoning steps

## 🔒 Dataset Privacy Notice

The dataset used in this project is private and **cannot be publicly shared** due to ethical considerations and user privacy concerns. Please contact the project author for questions regarding data access for academic collaboration only.

## 🙏 Acknowledgements

I would like to thank the **SSTP Program** and the **University of Iowa Belin-Blank Center** for providing me with this invaluable research opportunity. I am especially grateful to **Dr. Weiguo (Patrick) Fan** and the **Business Analytics Lab** for their support and for granting access to the Reddit dataset used in this study. Finally, I would like to thank **Enos Hsiao** and **Angelina Wang** for their assistance in annotating the original dataset.

## 📄 License

This project is for academic and research purposes only.


