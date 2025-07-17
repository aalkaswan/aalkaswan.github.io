---
title: "Code Red! On the Harmfulness of Applying Off-the-shelf Large Language Models to Programming Tasks"
authors: ["Ali Al-Kaswan", "Sebastian Deatc", "Begüm Koç", "Arie van Deursen", "Maliheh Izadi"]
date: "2025-06-19"
categories: ["Pre-trained Language Models", "Security", "AI Safety"]
weight: 7
---

# Abstract

Nowadays, developers increasingly rely on solutions powered by Large Language Models (LLM) to assist them with their coding tasks. This makes it crucial to align these tools with human values to prevent malicious misuse. In this paper, we propose a comprehensive framework for assessing the potential harmfulness of LLMs within the software engineering domain. We begin by developing a taxonomy of potentially harmful software engineering scenarios and subsequently, create a dataset of prompts based on this taxonomy. To systematically assess the responses, we design and validate an automatic evaluator that classifies the outputs of a variety of LLMs both open-source and closed-source models, as well as general-purpose and code-specific LLMs. Furthermore, we investigate the impact of models' size, architecture family, and alignment strategies on their tendency to generate harmful content.

## Links

{{< button href="https://dl.acm.org/doi/abs/10.1145/3663529.3663864" >}}📄 Full Paper{{< /button >}}

{{< button href="https://github.com/AISE-TUDelft/CodeRed" >}}💻 Replication Package{{< /button >}}

{{< button href="https://huggingface.co/spaces/AISE-TUDelft/Code-Red-Benchmark" >}}🤗 Huggingface Space{{< /button >}}
