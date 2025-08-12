# Income Qualification Prediction – Latin America (Costa Rica Household Data)

## 📌 Project Overview
This project predicts the **level of poverty (Level 1–4)** for households in Latin America using observable attributes (walls, ceilings, household assets, etc.). The aim is to improve the **Proxy Means Test (PMT)** used for subsidy allocation.

> **Goal:** Identify whether a person/household falls into a poor category (requiring subsidy) and determine their **poverty level**.

This implementation uses:
- Python **3.9**
- **Anaconda Navigator** 2.1.1, **Conda** 4.10.3
- **Pandas**, **NumPy**, **Imblearn**,**seaborn**

---

## 📂 Data Source
The dataset used in this project originates from the **Inter-American Development Bank (IDB)** and is publicly available through the **Kaggle competition**:

**Costa Rican Household Poverty Level Prediction**  
[Kaggle Dataset Link](https://www.kaggle.com/competitions/costa-rican-household-poverty-prediction)

The dataset includes:
- **train.csv** – 9,557 rows, 143 features including the `Target` label.
- **test.csv** – 23,856 rows, same features without the `Target` label.
- Features describe household attributes such as construction materials, access to utilities, education levels, and asset ownership.

**Note:** In this repository, the original dataset files are **not** included due to company policy restrictions.


### Key Details:
- **train.csv** – training dataset with target variable (`Target`)
- **test.csv** – test dataset without target
- `idhogar` – household head identifier
- `Target` – poverty level (1: Extreme Poverty, 2: Moderate Poverty, 3: Vulnerable, 4: Non-poor)

---

## 🔍 Problem Statement
Many social programs struggle to correctly identify the poorest segment of the population, especially when income and expense records are missing. This project uses **machine learning** to improve classification accuracy for subsidy allocation.

---

## 🛠 Steps Performed
1. **Data Understanding & Cleaning**
   - Null handling to avoid ineffective ML training.
   - Merging `train` and `test` datasets (null targets in test).
   - Checking duplicate rows.
2. **Feature Engineering**
   - Identifying numerical and categorical features.
   - Filling numerical null values with column mean.
   - One-hot encoding categorical variables (<= 10 categories).
3. **Bias Detection**
   - Checking class imbalance.
   - Household-level poverty consistency checks.
   - Identifying houses without a head (`parentesco1`).
4. **Model Development**
   - Functions written to:
     - Print data info
     - Get numerical columns
     - Fill nulls
     - Encode categorical features
5. **Exporting Results**
   - Saving notebook outputs as `.py` or `.html`.

---

# Install dependencies
pip install -r requirements.txt

