# PowerEstimationNetworks

**Power Estimation Networks (PENs)** is a device-agnostic framework for predicting deep neural network (DNN) power consumption from architecture representations. The goal is to support generalisation to unseen and out-of-distribution architectures (e.g., MLP → CNN → RNN) using structured topology representations, adaptive embeddings, and predictor models.

This repository contains research code developed for a PhD thesis and includes continual-learning baselines (e.g., Progressive Neural Networks) alongside standard regression approaches.

## What this repo does
- Learns to predict power metrics from a **textual representation of a DNN architecture**.
- Supports experimentation with different modelling strategies:
  - continual learning (Progressive Neural Networks as a case study/baseline)
  - fine-tuning approaches
  - baseline regression models
- Designed to be **dataset-agnostic**: it can be used with any dataset that follows the same protocol as ABCD.

## Data format
The processed dataset is tabular and contains:
- **Input column:** `Model` (textual representation of the DNN architecture)
- **Target column:** `Avg_Power_Simpson` (power-related metric)

See [`data/README.md`](data/README.md) for details.

> Note: Raw datasets/traces may be hosted in institutional storage (e.g., a university data centre). This repository may include a processed subset suitable for running experiments.


## Quickstart
This project was originally developed in Google Colab. A minimal workflow is:

1. Clone the repository:
   ```bash
   git clone https://github.com/cengizmehmet/PowerEstimationNetworks.git
   cd PowerEstimationNetworks
   
2. Add your notebook to notebooks/ (or open it in Colab).
3. Place the dataset in: data/

If you later export the code into Python modules, we recommend adding:
- requirements.txt or pyproject.toml
- scripts/train.py and scripts/eval.py

## Reproducibility
For reproducible experiments, document:
- random seed(s)
- library versions
- dataset version/checksum
- train/val/test split protocol

## Citation
If you use this code in academic work, please cite it. See <a>CITATION.cff</a>


