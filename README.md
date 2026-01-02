# Zero-Shot vs. Specialized Forecasting: A Comparative Paradigm Study

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/release/python-3100/)
[![Paper Status](https://img.shields.io/badge/Status-Research%20Preview-green)](https://github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📖 Abstract
Time series forecasting has traditionally relied on **specialized learning**: training models like ARIMA or XGBoost on task-specific data. This approach, while effective, is resource-intensive and lacks transferability. The emergence of **Foundation Models** suggests a new paradigm: **Zero-Shot Generalization**, where a pre-trained model forecasts unseen data distributions without any fine-tuning.

This repository conducts a rigorous empirical evaluation of this paradigm shift. We benchmark a representative **Decoder-Only Foundation Model (TimesFM)** in a strictly zero-shot setting against established **Specialized Methods (XGBoost, LSTM)**.

## 🏆 Key Results

Preliminary results on the M5 Retail dataset indicate that the Foundation Model approach can outperform traditional supervised learning without task-specific training.

| Dataset | Metric | TimesFM (Zero-Shot) | XGBoost (Supervised) | Delta |
| :--- | :--- | :--- | :--- | :--- |
| **M5 (Retail)** | **MASE** | **1.2306** | 1.7944 | **-31.4% (Better)** |
| **M5 (Retail)** | sMAPE | 180.52% | 138.39% | +30.4% |
| **M4 (General)** | MASE | 1.4264 | *Pending* | -- |

## 📂 Repository Contents

* `notebooks/`: Jupyter/Colab notebooks containing the end-to-end experiments.
* `data/`: Datasets used for bechmarking (M4, M5, Traffic, ETTh1, Exchange).
* `results/`: Generated metrics.
