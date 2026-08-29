# Beyond Point Forecasts: A Survey on Probabilistic Forecasting for Time Series and Spatiotemporal Data

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains the empirical benchmarks, codes, and figures for the paper **"A Survey on Probabilistic Time Series and Spatiotemporal Forecasting: Methods, Practical Guidance, and Open Challenges"** by Donia Besher, Rajdeep Pathak, Madhurima Panja, and Tanujit Chakraborty.

## 📖 Overview

Probabilistic forecasting quantifies predictive uncertainty, which is essential for high-stakes decision-making in domains such as epidemiology, energy, transportation, and environmental science. While current literature typically isolates temporal and spatiotemporal domains, this survey bridges the gap by establishing a cohesive taxonomy that systematically organizes the entire spectrum of existing methodologies.

This repository supports the survey by providing unified empirical evaluations of representative methods, analyzing key trade-offs across predictive accuracy and computational efficiency.

### Taxonomy Highlights
*   **Model-Agnostic Methods:** Pre-control limits, Ensemble-based methods, and Distribution-free calibration (Conformal Prediction, Conformalized Quantile Regression).
*   **Model-Intrinsic Methods:** Bayesian Modeling (Hierarchical, State Space, Nonparametric, BNNs), Parametric Predictive Distributions, Distributional Regression (Quantile Regression, Engression, Loss-Driven), and Generative Models (Copulas, HMMs, VAEs, GANs, Normalizing Flows, Diffusion Models).
*   **Foundation Models:** Exploration of zero-shot uncertainty quantification in modern temporal foundation models.

## 🗂️ Repository Structure

The repository is organized to separate the benchmark codebase from the visualization and forecast data:

```text
├── Experiments/
│   └── Benchmark_Experiments.ipynb  # Contains the code for the empirical benchmark evaluations
├── Figures/
│   ├── Figure_Generators.ipynb      # Notebook for generating the figures used in the survey
│   ├── Forecasts/                   # Benchmark forecast files saved as .npz arrays
│   └── [Figure Image Files]         # Exported figures supporting the paper
├── LICENSE                          # MIT License
└── README.md                        # This file
```

### Experiments
*   `Experiments/Benchmark_Experiments.ipynb`: This core notebook executes the empirical benchmark of representative probabilistic forecasting methods under a unified protocol. It contains the data loading, model initialization, training loops, and evaluation metrics computation.

### Figures & Visualizations
*   `Figures/Figure_Generators.ipynb`: Generates the visualizations and comparative plots featured in the survey based on the benchmark results.
*   `Figures/Forecasts/`: Contains the raw output forecasts from the benchmarked models. These are serialized as `.npz` (NumPy zipped arrays) to ensure efficient storage and easy loading for post-processing and figure generation.

## 📊 Evaluation Metrics

The benchmark evaluates both point and probabilistic metrics, emphasizing calibration and sharpness, including:
*   Continuous Ranked Probability Score (CRPS)
*   Winkler Score
*   Prediction Interval Coverage Probability (PICP)
*   Pinball Loss

## 📝 Citation

If you find this survey, code, or benchmark useful in your research, please consider citing our paper:

```bibtex
@article{besher2026probabilistic,
  title={Beyond Point Forecasts: A Survey on Probabilistic Forecasting for Time Series and Spatiotemporal Data},
  author={Besher, Donia and Pathak, Rajdeep and Panja, Madhurima and Chakraborty, Tanujit},
  journal={Preprint},
  year={2026}
}
```
