---
title: "The Poisoned Chalice of LLM Evaluation Report"
authors: ["Jonathan Katzy", "Ali Al-Kaswan", "Razvan Mihai Popescu", "Zhou Yang"]
date: "2026-07-05"
categories: ["Pre-trained Language Models"]
weight: 3
---

# Abstract

Large language models are increasingly used to evaluate and support software engineering tasks, yet the validity of these evaluations is often undermined by uncertainty about whether benchmark instances were seen during pretraining. This can lead to data contamination, which may inflate performance and result in misleading conclusions about model capability. Despite this, the training corpora of many modern models are only partially disclosed, making direct decontamination infeasible. This creates a need for practical methods that can detect a large language models' prior exposure to training data without access to the full training corpus.
To address this challenge, we organize the first Poisoned Chalice of LLM Evaluation Competition, co-located with the FSE-AIWare 2026 Competition Track. The competition frames contamination detection as a white-box membership inference task on source code and provides participants with curated datasets, target models, baseline attacks, and a final evaluation on a held-out model and dataset. This design encourages methods that generalize beyond superficial dataset artifacts and beyond a single training setting.
This paper reports the setup and results of the competition. More broadly, the competition aims to catalyze the community around trustworthy LLM evaluation for software engineering.

## Links

{{< button href="https://dl.acm.org/doi/abs/10.1145/3803437.3807733" >}}📄 Competition Report{{< /button >}}
