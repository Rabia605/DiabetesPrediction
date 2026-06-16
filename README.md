# Diabetes Progression Prediction

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Type-Regression-9B59B6?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge"/>
</p>

<p align="center">
  A regression project predicting diabetes disease progression comparing <b>Linear Regression, Ridge, Lasso & Random Forest</b> with full EDA, feature scaling, and model evaluation.
</p>

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Models Used](#models-used)
- [Results](#results)
- [Tech Stack](#tech-stack)
- [How to Run](#how-to-run)
- [Project Structure](#project-structure)
- [Author](#author)

---

## Overview

This project applies **supervised regression** to the **sklearn Diabetes Dataset** to predict disease progression one year after baseline using patient health metrics. Four regression models are trained, evaluated, and compared using RMSE, MAE, and R².

---

**Features:**

| Feature | Description |
|:---|:---|
| age | Age of patient |
| sex | Sex of patient |
| bmi | Body mass index |
| bp | Average blood pressure |
| s1 | Total serum cholesterol |
| s2 | Low-density lipoproteins |
| s3 | High-density lipoproteins |
| s4 | Total cholesterol / HDL |
| s5 | Log of serum triglycerides level |
| s6 | Blood sugar level |

---

| Step | Description |
|:---:|:---|
| 1 | Load Diabetes dataset as DataFrame |
| 2 | Basic info, null & duplicate check |
| 3 | Target distribution, boxplots, histograms, scatterplots |
| 4 | 80/20 Train-Test Split (`random_state=42`) |
| 5 | StandardScaler applied to features |
| 6 | Four regression models trained |
| 7 | Evaluated on RMSE, MAE, R² |
| 8 | Best model identified and reported |

---

## Exploratory Data Analysis

| Analysis | Method |
|:---|:---|
| Data Overview | `.head()`, `.describe()`, `.shape`, `.info()` |
| Null Check | `.isnull().sum()` |
| Duplicate Check | `.duplicated().sum()` |
| Target Distribution | Histogram + Boxplot |
| Feature Boxplots | All features visualized |
| Scatter Analysis | Target vs Blood Pressure |
| Feature Correlation | Heatmap (`seaborn`, `coolwarm` palette) |
| Model Comparison | Bar plot of RMSE across models |

---

## Models Used

| Model | Library | Key Parameters |
|:---|:---|:---|
| Linear Regression | `sklearn.linear_model` | Default |
| Ridge Regression | `sklearn.linear_model` | `alpha=1.0` |
| Lasso Regression | `sklearn.linear_model` | `alpha=0.01, max_iter=10000` |
| Random Forest | `sklearn.ensemble` | `n_estimators=300, random_state=42` |

> Feature scaling applied using `StandardScaler` before model training.

---

## Results

| Model | RMSE ↓ | MAE ↓ | R² ↑ |
|:---|:---:|:---:|:---:|
| **Ridge Regression**  | **53.78** | **42.81** | **0.454** |
| Lasso Regression | 53.84 | 42.80 | 0.453 |
| Linear Regression | 53.85 | 42.79 | 0.453 |
| Random Forest | 54.92 | 44.75 | 0.431 |

> ↓ Lower is better &nbsp;|&nbsp; ↑ Higher is better

**Best Model → Ridge Regression** — lowest RMSE and highest R² score on this dataset.

---

## Tech Stack

| Tool | Purpose |
|:---|:---|
| Python | Core language |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Visualization |
| Seaborn | Statistical plots |
| Scikit-learn | ML models & evaluation |
| Jupyter Notebook | Development environment |

---

## How to Run

**1. Clone the repository**
```bash
git clone https://github.com/Rabia605/DiabetesPrediction.git
cd DiabetesPrediction
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Launch Jupyter Notebook**
```bash
jupyter notebook diabetes.ipynb
```

**4. Run all cells**

`Kernel` → `Restart & Run All`

---

## Project Structure

```
DiabetesPrediction/
│
├── diabetes.ipynb
├── README.md
└── requirements.txt
```

---

## Author

**Rabia Noreen**
*Software Engineer | Building with AI & ML*



---

<p align="center">If this project inspired you, hit that ⭐ button!</p>
