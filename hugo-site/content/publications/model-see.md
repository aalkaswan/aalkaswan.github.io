---
title: "Model See, Model Do? Exposure-Aware Evaluation of Bug-vs-Fix Preference in Code LLMs"
authors: ["Ali Al-Kaswan", "Claudio Spiess", "Prem Devanbu", "Arie van Deursen", "Maliheh Izadi"]
date: "2025-06-19"
categories: ["Pre-trained Language Models", "Security", "AI Safety"]
weight: 7
---

# Abstract

Large language models are increasingly used for code generation and debugging, but their outputs can still contain bugs, that originate from training data. Distinguishing whether an LLM prefers correct code, or a familiar incorrect version might be influenced by what it's been exposed to during training. We introduce an exposure-aware evaluation framework that quantifies how prior exposure to buggy versus fixed code influences a model's preference. Using the ManySStuBs4J benchmark, we apply Data Portraits for membership testing on the Stack-V2 corpus to estimate whether each buggy and fixed variant was seen during training. We then stratify examples by exposure and compare model preference using code completion as well as multiple likelihood-based scoring metrics We find that most examples (67%) have neither variant in the training data, and when only one is present, fixes are more frequently present than bugs. In model generations, models reproduce buggy lines far more often than fixes, with bug-exposed examples amplifying this tendency and fix-exposed examples showing only marginal improvement. In likelihood scoring, minimum and maximum token-probability metrics consistently prefer the fixed code across all conditions, indicating a stable bias toward correct fixes. In contrast, metrics like the Gini coefficient reverse preference when only the buggy variant was seen. Our results indicate that exposure can skew bug-fix evaluations and highlight the risk that LLMs may propagate memorised errors in practice.

## Links

{{< button href="https://arxiv.org/pdf/2601.10496" >}}📄 Pre-print{{< /button >}}


