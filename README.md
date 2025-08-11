# 🚢 Task 5 - Exploratory Data Analysis (EDA) on Titanic Dataset

## 📌 Project Overview
This project is part of **Task 5** for the Data Analysis course.  
The objective is to perform **Exploratory Data Analysis (EDA)** on the Titanic dataset to explore patterns, detect relationships, and identify key factors influencing survival rates.

---

## 📂 Files in this Repository
- **Task5_EDA_Titanic.ipynb** — Google Colab Jupyter Notebook with complete EDA process.
- **Task5_EDA_Titanic.pdf** — Exported PDF of the notebook for quick review.
- **README.md** — Project documentation.
- *(Optional)* `train.csv` dataset if permitted to upload.
- **requirements.txt** — Python dependencies to run the notebook.

---

## 🛠 Tools & Libraries Used
- **Python** — Programming language for analysis
- **pandas** — Data manipulation
- **numpy** — Numerical computations
- **matplotlib** & **seaborn** — Data visualization
- **scikit-learn** — Data preprocessing
- **statsmodels** — Statistical analysis (VIF calculation)

---

## 📊 EDA Steps Performed

### 1. Data Understanding
- Loaded Titanic dataset (`train.csv`)  
- Inspected structure, data types, and descriptive statistics.

### 2. Data Cleaning
- Handled missing values:
  - Filled `Age` with median.
  - Filled `Embarked` with mode.
  - Created `HasCabin` flag for `Cabin` presence.
- Verified no duplicates.
  
### 3. Feature Engineering
- Created:
  - `FamilySize` = `SibSp` + `Parch` + 1
  - `Title` extracted from passenger names
  - `Fare_log` (log transformation to handle skewness)
  - `Age_bin` (categorized ages into groups: child, teen, adult, mid, senior)

### 4. Univariate Analysis
- Count plots for **Pclass**, **Sex**, and **Survived**.
- Histograms for **Age** and **Fare_log** distributions.

### 5. Bivariate Analysis
- Survival rate comparisons by **Sex** and **Pclass**.
- Boxplots for **Age** vs **Survived**.
- Bar plots for **Pclass** vs survival rate.

### 6. Multivariate Analysis
- Pairplots of numerical features colored by survival.
- Correlation heatmap to find relationships between numerical variables.

### 7. Statistical Checks
- Calculated skewness for numeric columns.
- Checked multicollinearity using **Variance Inflation Factor (VIF)**.

---

## 🔍 Key Insights
- **Gender**: Females had much higher survival rates than males.
- **Pclass**: First-class passengers had the highest survival rates.
- **Age**: Younger passengers had better survival chances.
- **FamilySize**: Extremely small or large family sizes reduced survival chances.
- High VIF values for `SibSp`, `Parch`, and `FamilySize` indicate correlation between them.

---

## 🚀 How to Run the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/Task5_EDA_Titanic.git
   cd Task5_EDA_Titanic

