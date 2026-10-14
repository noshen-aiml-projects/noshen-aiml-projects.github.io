---
layout: page
title: Pipeline Tag Prediction from Model Cards
description: Fine-tuned RoBERTa and ModernBERT to predict a Hugging Face model's task from its model card text. Paper included.
importance: 1
category: work
---

**UC Berkeley MIDS · DATASCI 266 (NLP) · 2026** — with Novejot Kaur Bal · [Code on GitHub](https://github.com/noshen-aiml-projects/HF_Pipeline_Tag)

<p>
  <a
    href="{{ '/assets/pdf/pipeline_tag_prediction.pdf' | relative_url }}"
    target="_blank"
    rel="noopener"
    style="display: inline-block; padding: 0.5rem 1.1rem; border: 1px solid var(--global-theme-color); border-radius: 6px; color: var(--global-theme-color); font-weight: 500; text-decoration: none"
  >
    <i class="fa-solid fa-file-pdf"></i>&nbsp; Read the paper (PDF)
  </a>
</p>

The Hugging Face Hub hosts over 1.4 million models, but the `pipeline_tag` that declares each model's primary task is self-reported, and in our July 2026 crawl of 667,424 model repositories, 49.4% had no tag at all. We asked whether a model's task can be predicted from its model card text alone, so missing metadata could be recovered automatically at scale.

- Built a cleaned dataset of 145,003 labeled model cards: removed duplicates and boilerplate templates, applied text-quality thresholds, and stripped the YAML metadata block so models couldn't simply pattern-match the label.
- Compared a TF-IDF + logistic regression baseline against fine-tuned **RoBERTa** and **ModernBERT** on the ten most frequent pipeline tags. ModernBERT reached **96.54% accuracy and 0.964 macro-F1**, ahead of RoBERTa (0.954), the baseline (0.952), and the 0.935 F1 reported in the prior work that motivated the study.
- Ran a data-scaling ablation (25/50/75/100% of training data): ModernBERT overtook the baseline from 50% of the data onward, while RoBERTa needed the full set.
- Applied all three models to **115,620 previously untagged model cards**. The fine-tuned transformers were far more confident than the baseline (~90% vs. 64% mean confidence), and RoBERTa and ModernBERT agreed on 87.0% of cards, a proxy signal that the gains generalize beyond the labeled test set.

## Paper

<div class="paper-embed">
  <object data="{{ '/assets/pdf/pipeline_tag_prediction.pdf' | relative_url }}#navpanes=0&view=FitH" type="application/pdf" width="100%" style="height: 85vh; min-height: 600px; border: 1px solid var(--global-divider-color); border-radius: 6px">
    <p>
      Your browser can't display the PDF here.
      <a href="{{ '/assets/pdf/pipeline_tag_prediction.pdf' | relative_url }}" target="_blank" rel="noopener">Open the paper (PDF)</a> instead.
    </p>
  </object>
</div>
