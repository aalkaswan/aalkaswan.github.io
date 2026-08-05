---
title: "Do Agents Dream of Root Shells? Partial-Credit Evaluation of LLM Agents in Capture The Flag Challenges"
authors: ["Ali Al-Kaswan", "Maksim Plotnikov", "Maxim Hájek", "Roland Vízner", "Arie van Deursen", "Maliheh Izadi"]
date: "2026-04-21"
categories: ["LLM Agents", "Security", "Benchmarks"]
weight: 8
---

# Abstract

Large Language Model (LLM) agents are increasingly proposed for autonomous cybersecurity tasks, but their capabilities in realistic offensive settings remain poorly understood. We present DeepRed, an open-source benchmark for evaluating LLM-based agents on realistic Capture The Flag (CTF) challenges in isolated virtualized environments. DeepRed places an agent in a Kali attacker environment with terminal tools and optional web search, connected over a private network to a target challenge, and records full execution traces for analysis. To move beyond binary solved/unsolved outcomes, we introduce a partial-credit scoring method based on challenge-specific checkpoints derived from public writeups, together with an automated summarise-then-judge labelling pipeline for assigning checkpoint completion from logs. Using DeepRed, we benchmark ten commercially accessible LLMs on ten VM-based CTF challenges spanning different challenge categories. The results indicate that current agents remain limited: the best model achieves only 35% average checkpoint completion, performing strongest on common challenge types and weakest on tasks requiring non-standard discovery and longer-horizon adaptation.

## Links

{{< button href="https://dl.acm.org/doi/pdf/10.1145/3805760.3814926" >}}📄 Full Paper{{< /button >}}

{{< button href="https://github.com/AISE-TUDelft/DeepRed-LLMAgent" >}}💻 Replication Package{{< /button >}}