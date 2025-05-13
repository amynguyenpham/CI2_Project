# CI2_Project

# CI2 Final Project: Causal Transportability of Harmful Content Classification

This repository contains code and artifacts for the final project in COMS 4995: Causal Inference 2. The goal is to evaluate and improve the generalizability of hate speech classifiers across social media platforms using causal transportability techniques.

---

## 📁 Source Data

- **Original dataset**: [UCB D-Lab Measuring Hate Speech](https://huggingface.co/datasets/ucberkeley-dlab/measuring-hate-speech)
- **Processed files**:
  - `train.csv`
  - `train_with_topics.csv`
  - `test_reddit.csv`
  - `test_youtube.csv`

---

## ⚙️ Training Notebooks

### 1. `Project_P(YgivenX).ipynb`
- **Task**: Standard classifier P(Y|X) using BERT.
- **Model**: [BERT](https://huggingface.co/docs/transformers/en/model_doc/bert)
- **Training framework**: [Hugging Face Trainer](https://huggingface.co/transformers/v3.1.0/training.html#trainer)

**Output**:  
- `Project_P(YgivenX).pdf`: Report summarizing training results.

---

### 2. `Project_P(YgivenX,A).ipynb`
- **Task**: Standard classifier trained on both `X` (text) and `A` (topic) (P(Y|X,A)).
- **Model**: [BERT](https://huggingface.co/docs/transformers/en/model_doc/bert)
- **Trainer**: [Hugging Face Trainer](https://huggingface.co/transformers/v3.1.0/training.html#trainer)

---

## 🌐 In-Domain Classifiers using P(Y \| do(X))

These notebooks estimate the interventional distribution \( P^*(Y \mid \text{do}(X)) \) using:
- **P\*(A)**: Generated via [FLAN-T5-BASE](https://huggingface.co/google/flan-t5-base)
- **P(Y \| X, A)**: Precomputed from `Project_P(YgivenX,A).ipynb`

Training results are noted in the notebook

### 3. `P(Y_do(x))_Twitter_In_Domain.ipynb`
- In-domain classifier for Twitter.

### 4. `P_(Y_do(x)_Youtube.ipynb`
- In-domain classifier for YouTube.

### 5. `P_(y_do(x)_Reddit.ipynb`
- In-domain classifier for Reddit.
