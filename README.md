# Politeness-TBBT-NLP
Automated classification of Leech's Politeness Maxims in 'The Big Bang Theory' dialogue using DistilBERT, SVM, and Logistic Regression.
## Project Overview"
This project explores the computational modeling of interpersonal pragmatics. Based on **Geoffrey Leech’s (1983) Politeness Principle**, we classified sitcom dialogues into four maxims: **Tact, Agreement, Approbation, and Sympathy**. Our goal was to evaluate how well transformer-based models capture social nuances compared to traditional machine learning methods."

## Key Features
* **Dataset & Context**
  * Source: TBBT transcripts (46,000+ lines).
  * Window size: 5 consecutive utterances.
  * Anonymization: Character names replaced to reduce bias.
* **Models Implemented**
  * Traditional: Logistic Regression & SVM (TF-IDF).
  * Deep Learning: Fine-tuned **DistilBERT**.

## Results Summary
We evaluated our models on the **Joint-Consolidated Data (Test Set)**. While the Majority Baseline achieved high accuracy due to class imbalance, **DistilBERT** significantly outperformed other models in **Macro-F1**, proving its ability to capture pragmatic nuances.

| Model | Feature Representation | Test Accuracy | **Test Macro-F1** |
| :--- | :--- | :---: | :---: |
| Majority Baseline | Frequency-based | 0.710 | 0.166 |
| Logistic Regression | BOW | 0.700 | 0.203 |
| Logistic Regression | TF-IDF | 0.720 | 0.247 |
| SVM | BOW | 0.600 | 0.284 |
| SVM | TF-IDF | 0.680 | 0.331 |
| **DistilBERT** | **Contextual Embeddings** | **0.720** | **0.533** |

> **Note:** The high Macro-F1 of DistilBERT indicates its superior performance in identifying minority classes like *Sympathy* and *Approbation* compared to traditional keyword-based models.

## Authors
* Huanyu Dong
* Joel Vázquez
* Nora Grunditz
* Yu Chien Lin
