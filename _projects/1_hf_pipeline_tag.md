---
layout: page
title: Pipeline Tag Prediction from Model Cards
description: Fine-tuned RoBERTa and ModernBERT to predict a Hugging Face model's task from its model card text.
importance: 1
category: work
---

**UC Berkeley MIDS · DATASCI 266 (NLP) · 2026** — with Novejot Kaur Bal · [Code on GitHub](https://github.com/noshen-aiml-projects/HF_Pipeline_Tag)

The Hugging Face Hub hosts over a million models, but the `pipeline_tag` that declares each model's primary task is self-reported and often missing. We asked whether a model's task can be predicted from its model card text alone, so missing metadata could be recovered automatically at scale.

- Built a cleaned dataset of ~145K labeled model cards from a Hugging Face snapshot of ~686K cards: removed duplicates and boilerplate templates, applied a text-quality threshold, and stripped the YAML metadata block so models couldn't simply pattern-match the label.
- Compared a TF-IDF + logistic regression baseline against fine-tuned **RoBERTa** and **ModernBERT** on the top ten pipeline tags, evaluated with accuracy and macro-F1.
- Performance improved from the baseline to RoBERTa to ModernBERT, and improved on the prior work that motivated the study.
- Ran a data-scaling ablation (25/50/75/100% of training data) to estimate how much labeled data a reliable model-recommendation system needs, and tested generalization on unlabeled model cards.
