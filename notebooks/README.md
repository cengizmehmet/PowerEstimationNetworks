# Continual Learning on Unseen Data for Power Prediction

This repository contains the **continual learning experiments from Chapter 5** of my PhD thesis.  
The study evaluates how different learning paradigms handle **previously unseen data**, with a particular focus on **efficiency, robustness, and generalisation** rather than raw performance alone.

Unlike traditional benchmarks, the experiments here are designed to **challenge common assumptions** behind:
- Transfer Learning
- Continual Learning
- Standard deep neural networks trained in isolation

by analysing their behaviour under **incremental exposure to new, out-of-distribution data**.

---

## 🔍 Research Motivation

In many real-world settings, models are deployed in environments where:
- new data distributions emerge over time,
- unseen patterns cannot be anticipated during initial training,
- retraining from scratch is expensive or impractical.

This work investigates whether commonly used learning paradigms are **actually efficient** at handling such scenarios, particularly when the cost of adaptation and stability under distributional shift are taken into account.

---

## 🧠 Experimental Overview

The experiments implement a **continual learning protocol** consisting of multiple training blocks:

- **Block 1 – Baseline (Training Data)**  
  A model trained solely on the original training split.

- **Block 2 – Continual Extension (Unknown Data)**  
  The model is extended to accommodate previously unseen data, with controlled vocabulary expansion and partial parameter reuse.

- **Block 3 – Merged Learning (Seen + Unseen)**  
  Training is performed on a merged dataset to assess stability and performance when both known and unknown data coexist.

Each block is evaluated independently on:
- seen data
- unseen data
- merged distributions

This allows a direct comparison of **adaptation efficiency** and **generalisation behaviour** across learning stages.

---
