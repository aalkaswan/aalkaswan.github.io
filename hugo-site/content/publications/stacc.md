---
title: "STACC: Code Comment Classification using SentenceTransformers"
authors: ["Ali Al-Kaswan", "Maliheh Izadi", "Arie van Deursen"]
date: "2023-02-25"
categories: ["Pre-trained Language Models"]
weight: 2
---

# Abstract

Code comments are a key resource for information about software artefacts. Depending on the use case, only some types of comments are useful. Thus, automatic approaches to classify these comments are proposed.
In this work, we address this need by proposing, STACC, a set of SentenceTransformers-based binary classifiers. 
These lightweight classifiers are trained and tested on the NLBSE Code Comment Classification tool competition dataset, and surpass the baseline by a significant margin, achieving an average F1 score of 0.74 against the baseline of 0.31, which is an improvement of 139%.
A replication package, as well as the models themselves, are publicly available

## Huggingface Space

<script type="module" src="https://gradio.s3-us-west-2.amazonaws.com/3.17.0/gradio.js"></script>
<gradio-app src="https://aise-tudelft-stacc.hf.space"></gradio-app>

## Links

{{< button href="https://arxiv.org/pdf/2302.07735.pdf" >}}📄 Full Paper{{< /button >}}

{{< button href="https://github.com/AISE-TUDelft/STACC" >}}💻 Replication Package{{< /button >}}

{{< button href="https://aise-tudelft-stacc.hf.space/" >}}🤗 Huggingface Space{{< /button >}}
