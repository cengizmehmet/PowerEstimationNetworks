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

## Dataset schema (common to all splits)

### Core fields
| Column name | Description |
|------------|-------------|
| Model | Textual representation of the DNN architecture (input feature). |
| Avg_Power_Simpson | Average power consumption computed using Simpson’s rule (primary regression target). |

### Current-related statistics (averaged over time)
| Column name | Description |
|------------|-------------|
| Avg_Current_mean | Mean current. |
| Avg_Current_median | Median current. |
| Avg_Current_standard_deviation | Standard deviation of current. |
| Avg_Current_variance | Variance of current. |
| Avg_Current_minimum | Minimum observed current. |
| Avg_Current_maximum | Maximum observed current. |
| Avg_Current_skewness | Skewness of current distribution. |
| Avg_Current_kurtosis | Kurtosis of current distribution. |

### Voltage-related statistics (averaged over time)
| Column name | Description |
|------------|-------------|
| Avg_Voltage_mean | Mean voltage. |
| Avg_Voltage_median | Median voltage. |
| Avg_Voltage_standard_deviation | Standard deviation of voltage. |
| Avg_Voltage_variance | Variance of voltage. |
| Avg_Voltage_minimum | Minimum observed voltage. |
| Avg_Voltage_maximum | Maximum observed voltage. |
| Avg_Voltage_skewness | Skewness of voltage distribution. |
| Avg_Voltage_kurtosis | Kurtosis of voltage distribution. |

### Power-related statistics (averaged over time)
| Column name | Description |
|------------|-------------|
| Avg_Power_mean | Mean power. |
| Avg_Power_median | Median power. |
| Avg_Power_standard_deviation | Standard deviation of power. |
| Avg_Power_variance | Variance of power. |
| Avg_Power_minimum | Minimum observed power. |
| Avg_Power_maximum | Maximum observed power. |
| Avg_Power_skewness | Skewness of power distribution. |
| Avg_Power_kurtosis | Kurtosis of power distribution. |


## Data availability

The authoritative version of the dataset is archived in the Newcastle University Data Centre. Access to information is provided in the PhD thesis (Chapter 4).



