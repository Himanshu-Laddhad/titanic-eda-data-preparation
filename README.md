# 🚢 Titanic — Data Understanding & Preparation

> **Course:** MGMT 59000V — Visual Analytics
> **Assignment:** Homework 1
> **Author:** Himanshu Laddhad

---

## Overview

This project applies a structured data analysis workflow to the classic **Titanic passenger dataset**. The focus is on understanding raw data quality, preparing it for downstream analysis, and making data-driven decisions — laying the groundwork for reliable visual storytelling.

---

## Dataset

| Property | Details |
|---|---|
| **Source** | [Kaggle – Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset) |
| **File** | `Titanic-Dataset.csv` |
| **Records** | 891 passengers |
| **Features** | 12 columns (PassengerId, Survived, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked) |

---

## Project Structure

```
HW1/
├── Himanshu_Laddhad_HW1_Visual_Analytics.ipynb   # Main analysis notebook
├── Titanic-Dataset.csv                            # Raw dataset
├── 590_A1Rubric.pdf                               # Assignment rubric
└── README.md
```

---

## Analysis Breakdown

### Part 1 — Data Quality Assessment (70%)

**A) Missingness Analysis**
- Quantified missing values per column (counts & percentages)
- Visualized missingness as a binary matrix to reveal structural patterns
- Key finding: `Cabin` (~77% missing), `Age` (~20% missing), `Embarked` (2 rows)

**B) Inconsistency & Outlier Detection**
- Validated categorical values against expected domains (`Pclass` ∈ {1,2,3}, `Sex` ∈ {male, female}, `Embarked` ∈ {C,Q,S})
- Applied IQR-based outlier detection across all numeric columns
- Flagged extreme `Fare` values (e.g., £512 first-class tickets)

**C) Data Preparation**
- Imputed `Age` using median imputation
- Dropped `Cabin` due to excessive missingness
- Filled `Embarked` with modal value
- Encoded categorical features (`Sex`, `Embarked`) for analysis readiness

### Part 2 — Decision-Making from Data (30%)

- Built summary visualizations (survival rate by class, sex, age group)
- Derived actionable insights from cleaned data
- Addressed trade-offs between imputation strategies and analysis validity

---

## Key Findings

- **Women and children first** — survival rate for females (~74%) was nearly 3× that of males (~19%)
- **Class matters** — 1st class passengers had a survival rate of ~63% vs ~24% for 3rd class
- **Age distribution** skewed young; children under 10 showed elevated survival rates
- **Fare outliers** concentrated exclusively in Pclass 1, validating data consistency

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core analysis language |
| Pandas | Data manipulation & cleaning |
| NumPy | Numerical computations |
| Matplotlib | Visualizations |
| Jupyter Notebook | Interactive analysis environment |

---

## How to Run

1. Clone or download this folder
2. Ensure `Titanic-Dataset.csv` is in the same directory as the notebook
3. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib jupyter
   ```
4. Launch the notebook:
   ```bash
   jupyter notebook Himanshu_Laddhad_HW1_Visual_Analytics.ipynb
   ```
5. Run all cells top-to-bottom

---

## Author

**Himanshu Laddhad**
PUID: 039494953
Purdue University — MGMT 59000V Visual Analytics
