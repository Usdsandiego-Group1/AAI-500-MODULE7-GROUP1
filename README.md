# AAI-500-MODULE7-GROUP1
AAI-500-MODULE7-GROUP1-PROJECT
by
OM BAVAL
GURUGANESH HEGDE
NAVEEN HN

# Health Risk Indicators & Insurance Premium Prediction

## Project Title
**Analyzing Health Risk Indicators and Predicting Insurance Premiums Using Statistical and Machine Learning Techniques**

## Objective
The goal of this project is to investigate how various health conditions and demographics influence annual health insurance premium prices. Using a dataset of 986 individuals, we apply descriptive statistics, inferential methods, and machine learning to:

- Explore variable relationships
- Perform hypothesis testing
- Build regression models for premium prediction
- Classify diabetes status
- Cluster users into health risk segments

---

## Dataset Overview

- **File**: `Medicalpremium.csv`
- **Instances**: 986 rows
- **Features**: 11 columns (all integers)
- **Key Columns**:
  - `Age`, `Diabetes`, `BloodPressureProblems`, `AnyChronicDiseases`
  - `Height`, `Weight`, `KnownAllergies`, `PremiumPrice`
  - `NumberOfMajorSurgeries`, `HistoryOfCancerInFamily`, `AnyTransplants`

The dataset is clean with no missing values and is suitable for statistical analysis and modeling.

---

## Methodology

### 1. Descriptive & Exploratory Data Analysis
- Five number summary, histograms, boxplots, pairplots
- Outlier detection and distribution analysis

### 2. Confidence Interval Estimation
- 95% CI for premium and BMI
- Prediction intervals
- Bayesian posterior for premium mean

### 3. Hypothesis Testing
- T-tests: Diabetes vs Premium, BMI > 25
- Z-test: Diabetes proportion ≠ 0.2

### 4. Regression Modeling
- Simple Linear Regression: Premium ~ Age
- Multiple Linear Regression: Premium ~ Age + BMI + Surgeries
- Generalized Linear Model (GLM)

### 5. Classification
- Random Forest to predict Diabetes
- Evaluation: Accuracy, Precision, Recall, AUROC, Confusion Matrix

### 6. Clustering
- KMeans on Age, BMI, Premium
- Cluster characterization and risk group segmentation

---

## Libraries Used

```python
pandas
numpy
matplotlib
seaborn
scipy
scikit-learn
statsmodels
```

> All listed in `requirements.txt`

---

## Key Results

### Insights from EDA & Hypothesis Testing:
- Premiums are significantly higher for diabetics (p < 0.01)
- Surgeries are positively correlated with premium costs
- BMI and premium show right-skewed distributions

### Regression:
- **Simple Linear Regression**: Age alone explains limited variation
- **Multiple Linear Regression**: R² ≈ 0.50 with Age, BMI, and Surgeries
- **GLM Output**: All predictors statistically significant (p < 0.001)

### Classification:
- **Random Forest Accuracy**: ~59%
- **Top Features**: BMI and Number of Surgeries
- **Evaluation Metrics**: Precision, Recall, F1 Score, AUROC
- **Confusion Matrix**: Captures imbalance in diabetic classification

### Clustering:
- Applied **KMeans** on standardized Age, BMI, and Premium
- **Three Clusters** Identified:
  - Cluster 0: Older, higher BMI, high premium (High Risk)
  - Cluster 1: Younger, lower BMI, low premium (Low Risk)
  - Cluster 2: Mixed demographic and risk

---

## File Structure
```
project-root/
├── Final Team Project Group 1.ipynb     # Jupyter notebook
├── Final Team Project Group 1.pdf       # PDF version
├── Medicalpremium.csv                   # Dataset
├── requirements.txt                     # Python dependencies
└── README.md                            # Project documentation
```

---

## 🚀 Getting Started

To set up and run the project locally:

1. **Clone or download** the repository.
2. **Install dependencies** using:
   ```bash
   pip install -r requirements.txt
3. **Launch the Jupyter Notebook**:
   ```bash
   jupyter notebook "Final Team Project Group 1.ipynb"
   
