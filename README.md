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

# Dataset access

This repository includes a lightweight, processed dataset suitable for demonstration and reproducibility purposes.

The complete dataset, including raw traces and intermediate artefacts, is hosted in the Newcastle University Data Centre and is available upon request or via institutional access.

For full dataset access, see:
<INSTITUTIONAL LINK HERE>

## Dataset schema
- Model: textual representation of the DNN architecture
- Avg_Power_Simpson: target power metric

Additional columns may include analytical descriptors and metadata.

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

## Related publications
This repository accompanies the following research outputs:

- **PhD thesis** (to appear):  
  *Generalising Performance Prediction via Incremental Topology Exploration of Deep Neural Networks and Continual Learning*,
  Mehmet Cengiz, Newcastle University.
  The full dataset is described in **Chapter 4**, and the study associated with this repository is presented in **Chapter 5**.

- **Journal / conference papers** (in preparation / under review):  
  Details will be added once available.

If you use this code or dataset, please cite the software (see [`CITATION.cff`](CITATION.cff)) and the corresponding publication when available.

## License
This project is released under the MIT License (see [`LICENSE`](LICENSE)).
