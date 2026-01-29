# 🧾 Catching the Rare: Ensemble and Linear Models for Imbalanced Network Intrusion Detection

![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18408605.svg)](https://doi.org/10.5281/zenodo.18408605)
![Python](https://img.shields.io/badge/python-3.11-blue)
![GitHub last commit](https://img.shields.io/github/last-commit/harddikk/Catching-the-Rare)
![GitHub issues](https://img.shields.io/github/issues/harddikk/Catching-the-Rare)

This repository contains the code and analysis accompanying the research paper  
**“Catching the Rare: Ensemble and Linear Models for Imbalanced Network Intrusion Detection.”**

The research has been **published on [Zenodo](https://zenodo.org/records/18408605)** (DOI: https://doi.org/10.5281/zenodo.18408605).

The paper is published on Zenodo (Version 2.0):  
https://doi.org/10.5281/zenodo.18408605

---

## Overview

Network intrusion detection is challenged by extreme class imbalance, where rare attack instances are easily overshadowed by benign traffic. This project investigates supervised machine learning approaches for binary intrusion detection, with an explicit focus on detecting minority (attack) classes rather than optimizing overall accuracy.

While the study is inspired by attack behaviors commonly analyzed in honeypot environments, it does not involve live honeypot deployment. Experiments are conducted using the publicly available CICIDS 2017 dataset, generated in a controlled environment that simulates realistic benign and malicious network traffic.

Core research focus:
- Linear vs ensemble models under class imbalance
- Precision–recall analysis over raw accuracy
- Feature importance and interpretability
- Transparent discussion of methodological limitations

**Goal:**  
> To improve early intrusion detection by identifying deceptive attack vectors through data-driven insights.

---

## ⚙️ Setup Instructions

**Clone the repo:**
```bash
git clone https://github.com/harddikk/Catching-the-Rare.git
cd Catching-the-Rare
```

**Install dependencies:**
```bash
pip install -r requirements.txt
```

---

## Dataset

This project uses the CICIDS 2017 intrusion detection dataset released by the Canadian Institute for Cybersecurity.

Due to size and licensing constraints, the dataset is not included in this repository.

To reproduce the experiments:
1. Download CICIDS 2017 from the official source
2. Place the extracted CSV files in a directory named:
```bash
CICIDS2017/
```
at the project root.

---

## 🗂 Project Structure

<details>
<summary>Click to expand</summary>

```
Catching-the-Rare/
├── honeypot_intrusion_detection.ipynb      # Main Jupyter Notebook
├── requirements.txt                        # Python dependencies
├── LICENSE                                 # CC BY 4.0 License
├── README.md                               # This file
├── CICIDS2017/                             # Dataset folder (not included)
└── results/                                # Folder for selected plots/images
    ├── confusion_matrix_rf.png
    └── feature_importance_rf.png
```

</details>

---

## 🚀 Running the Notebook

Open
```bash
honeypot_intrusion_detection.ipynb
```
in Jupyter Notebook or VS Code, and execute all cells sequentially.  
Results (plots, accuracy metrics, confusion matrices, etc.) will be displayed inline.

---

## 🧩 Techniques Used

- Data preprocessing and cleaning
- Stratified sampling under class imbalance
- Feature scaling with leakage-aware pipelines
- Supervised ML models:
  - Logistic Regression (linear baseline)
  - Random Forest (ensemble)
  - XGBoost (ensemble)
- Evaluation using imbalance-aware metrics:
  - Precision–Recall curves
  - ROC curves
  - Balanced accuracy


---

## 📈 Results

<details>
<summary>Click to expand: Model Performance Metrics & Plots</summary>

                                                          
| Model               | Accuracy | Precision (weighted) | Recall (weighted) | F1-Score (weighted) |
|--------------------|----------|--------------------|-----------------|-------------------|
| Logistic Regression | 0.9416   | 0.9489             | 0.9416          | 0.9435            |
| Random Forest       | 0.9986   | 0.9985             | 0.9986          | 0.9985            |
| XGBoost             | 0.9991   | 0.9991             | 0.9991          | 0.9991            |

> Note: Metrics are calculated on the test split of the dataset.  

**Selected plots:**

![Confusion Matrix (RF)](results/confusion_matrix_rf.png)  
![Feature Importance - Top 10 (RF)](results/feature_importance_rf.png)

> Note: Accuracy is reported for completeness but is not emphasized due to severe class imbalance.
> Confusion matrices for other models and feature importance for XGBoost are available in the notebook.

</details>

---

## 📚 Citation

If you use or reference this work, please cite:

```
Tiwari, Hardik. (2026). Catching the Rare: Ensemble and Linear Models for Imbalanced Network Intrusion Detection. Zenodo. https://doi.org/10.5281/zenodo.18408605
```

---

## 📄 License

This project is licensed under the **Creative Commons Attribution 4.0 International License**.  
You’re free to use, modify, and share it — just give proper credit.

---

## 👨‍💻 Author

Hardik Tiwari  
High school Researcher passionate about AI, cybersecurity, and system-level innovation.  
[Connect on LinkedIn](https://www.linkedin.com/in/harrdik-tiwari) 🚀
