# Interpretable Multi-Source Machine Learning for Urban Classification in Data-Scarce Regions

[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)]()
## Conference Poster

The final conference poster presented at **Deep Learning Indaba 2026** is available in the `poster/` directory.

## Overview

This repository accompanies the accepted paper:

> **Interpretable Multi-Source Machine Learning for Urban Classification in Data-Scarce Regions**

presented at the **Deep Learning Indaba (DLI) 2026**.

The study develops an interpretable machine learning framework for urban classification by integrating multi-source remote sensing, topographic, demographic, and night-time light datasets. Three machine learning models—Random Forest, XGBoost, and a Neural Network—are evaluated, while SHAP (SHapley Additive exPlanations) is employed to provide transparent explanations of model predictions.

The repository contains the complete Jupyter notebook, supporting figures, and the resources required to reproduce the analyses presented in the paper.

---

## Repository Structure

```text
interpretable-urban-classification/
│
├── notebooks/
│   └── Urban_Classification_Workflow.ipynb
│
├── data/
│   ├── urban_2000.csv
│   ├── urban_2005.csv
│   ├── urban_2010.csv
│   ├── urban_2015.csv
│   ├── urban_2020.csv
│   ├── urban_2024.csv
│   └── Lagos_full_stack_100m.tif
│
├── figures/
│   ├── Figure1_*.png
│   ├── Figure2_*.png
│   ├── Figure3_SHAP_Beeswarm.png
│   ├── Figure4_SHAP_Feature_Importance.png
│   ├── Figure5_SHAP_Dependence_NightLights.png
│   └── Figure6_Urban_Probability_2020.png
│
├── paper/
│
├── poster/
│
├── results/
│
├── README.md
├── LICENSE
├── requirements.txt
├── environment.yml
└── CITATION.cff
```

---

## Study Area

The study focuses on **Lagos, Nigeria**, one of Africa's fastest-growing metropolitan regions. Urban classification was performed using multi-temporal Earth observation and socio-economic datasets spanning **2000–2024**.

---

## Predictor Variables

The machine learning models were developed using ten predictor variables:

| Variable | Description |
|-----------|-------------|
| Blue | Landsat Blue Band |
| Green | Landsat Green Band |
| Red | Landsat Red Band |
| NIR | Near Infrared |
| SWIR | Shortwave Infrared |
| NDVI | Normalized Difference Vegetation Index |
| NDBI | Normalized Difference Built-up Index |
| NightLights | Night-time Light Intensity |
| Population | Population Density |
| Elevation | Digital Elevation Model |

The response variable is:

- **Urban**
  - 0 = Non-Urban
  - 1 = Urban

---

## Machine Learning Models

Three supervised learning models were evaluated:

- Random Forest
- XGBoost
- Neural Network (PyTorch)

Model interpretability was achieved using **SHAP (SHapley Additive exPlanations)**.

---

## Results

The Random Forest and XGBoost models achieved the strongest predictive performance, with ROC–AUC values exceeding **0.94**.

SHAP analysis identified **NightLights**, **NDBI**, **Population**, and **NDVI** among the most influential variables contributing to urban classification.

---

## Reproducing the Analysis

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/interpretable-urban-classification.git
```

Create the Conda environment:

```bash
conda env create -f environment.yml
```

Activate the environment:

```bash
conda activate geoenv
```

Launch Jupyter Lab:

```bash
jupyter lab
```

Open:

```
notebooks/Urban_Classification_Workflow.ipynb
```

Run all cells sequentially.

---

## Citation

If you use this repository, please cite:

> Ugege, P. (2026). *Interpretable Multi-Source Machine Learning for Urban Classification in Data-Scarce Regions*. Deep Learning Indaba (DLI 2026).

(Citation will be updated upon publication.)

---

## Contact

**Peter Ugege**

Forestry Research Institute of Nigeria (FRIN)

Email: *[add preferred contact email]*

---

## Acknowledgements

The authors acknowledge the Deep Learning Indaba (DLI) community for promoting open and reproducible artificial intelligence research across Africa.
