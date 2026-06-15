#  Diabetes Progression Prediction

A regression project that predicts diabetes disease progression using patient health metrics, comparing Linear Regression, Ridge, Lasso, and Random Forest models.

##  Overview

This project uses the sklearn Diabetes dataset to build and compare regression models for predicting disease progression. It covers the complete ML pipeline, data exploration, EDA, feature scaling, model training, and performance comparison.

##  Objective

To predict diabetes disease progression based on patient metrics like age, BMI, blood pressure, and serum measurements, and identify which regression model performs best.

##  Tech Stack

- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

##  Dataset

- **Source:** Diabetes dataset (`sklearn.datasets.load_diabetes`)
- **Features:** age, sex, bmi, bp, s1–s6 (blood serum measurements)
- **Target Variable:** target (a quantitative measure of disease progression one year after baseline)

##  Workflow

1. **Data Loading**  Loaded the sklearn Diabetes dataset into a DataFrame
2. **Data Exploration**  Checked shape, data types, summary statistics, and duplicates
3. **Exploratory Data Analysis (EDA)**  Visualized target distribution, feature boxplots, histograms, and scatterplots
4. **Correlation Analysis**  Used a heatmap to identify relationships between features and target
5. **Train-Test Split**  Split data into 80% training and 20% testing sets
6. **Feature Scaling**  Standardized features using `StandardScaler`
7. **Model Training**  Trained four regression models: Linear Regression, Ridge, Lasso, and Random Forest
8. **Model Evaluation**  Compared models using RMSE, MAE, and R² score

##  Models Compared
| Model | RMSE | MAE | R² |
|---|---|---|---|
| Ridge | 53.78 | 42.81 | 0.454 |
| Lasso | 53.84 | 42.80 | 0.453 |
| Linear Regression | 53.85 | 42.79 | 0.453 |
| Random Forest | 54.92 | 44.75 | 0.431 |


**Result:** Ridge Regression outperformed the other models on this dataset, making it the ideal choice for this scenario.

##  How to Run

```bash
# Clone the repository
git clone https://github.com/Rabia605/DiabetesPrediction.git

# Navigate to project directory
cd DiabetesPrediction

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook DiabetesPrediction.ipynb
```
