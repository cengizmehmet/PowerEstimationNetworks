# Dataset overview

This directory contains a lightweight, processed dataset used for training and evaluating Power Estimation Networks (PENs).

The complete dataset, including raw traces and intermediate artifacts, is hosted in the Newcastle University Data Centre and is not distributed via this repository.


## Dataset splits

- **train.csv**  
  Used for model training.

- **test.csv**  
  Held-out data used for evaluation on seen distribution(s).

- **unknown.csv**  
  Contains architectures not observed during training, used to assess generalisation and out-of-distribution performance.

## Schema (common to all splits)

| Column name | Description |
|------------|-------------|
| Model | Textual representation of the DNN architecture (input feature). |
| Avg_Power_Simpson | Average power consumption metric computed using Simpson’s rule (regression target). |

Additional columns may include analytical descriptors (e.g., FLOPs, parameter counts, activation memory) and metadata fields.

## Data availability

The authoritative version of the dataset is archived in the Newcastle University Data Centre. Access to information is provided in the PhD thesis (Chapter 4).



