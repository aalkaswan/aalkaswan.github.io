---
title: "Targeted Attack on GPT-Neo for the SATML Language Model Data Extraction Challenge"
authors: ["Ali Al-Kaswan", "Maliheh Izadi", "Arie van Deursen"]
date: "2023-02-17"
categories: ["Pre-trained Language Models"]
weight: 3
---

# Abstract

Previous work has shown that Large Language Models are susceptible to so-called data extraction attacks. This allows an attacker to extract a sample that was contained in the training data, which has massive privacy implications. The construction of data extraction attacks is challenging, current attacks are quite inefficient, and there exists a significant gap in the extraction capabilities of untargeted attacks and memorization. Thus, targeted attacks are proposed, which identify if a given sample from the training data, is extractable from a model. In this work, we apply a targeted data extraction attack to the SATML2023 Language Model Training Data Extraction Challenge. We apply a two-step approach. In the first step, we maximise the recall of the model and are able to extract the suffix for 69% of the samples. In the second step, we use a classifier-based Membership Inference Attack on the generations. Our AutoSklearn classifier achieves a precision of 0.841. The full approach reaches a score of 0.405 recall at a 10% false positive rate, which is an improvement of 34% over the baseline of 0.301.

## Links

{{< button href="https://arxiv.org/pdf/2302.07735.pdf" >}}📄 Full Paper{{< /button >}}
