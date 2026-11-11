# telecom_usage.csv
# 📊 Telecom Customer Churn – Data Preprocessing & Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project focuses on **Data Preprocessing and Exploratory Data Analysis (EDA)** using a Telecom Customer Usage dataset.

The main objective is to clean and prepare raw telecom customer data, identify patterns in customer usage, and explore the factors that may influence customer churn (customers leaving a telecom service).

Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn are used for data cleaning, preprocessing, statistical exploration, and visualization.

## 🎯 Objectives

- Understand the structure of the telecom dataset.
- Identify and handle missing values.
- Remove duplicate records and unnecessary columns.
- Convert incorrect data types into appropriate formats.
- Clean inconsistent categorical values and correct spelling mistakes.
- Encode categorical variables into numerical representations.
- Standardize numerical features.
- Detect and handle outliers.
- Perform univariate, bivariate, and multivariate analysis.
- Visualize customer usage patterns and churn distribution.

## 🛠️ Technologies & Libraries Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Feature scaling using StandardScaler |
| Google Colab | Development environment |
| GitHub | Project hosting and version control |

## 📂 Project Structure

```text
Telecom-Customer-Churn-EDA/
│
├── EDA.ipynb
├── telecom_usage_mixed.csv
├── telecom_churn_preprocessed.csv
└── README.md
```

## 🔍 Work Performed

### 1. Data Loading and Understanding
- Imported the required Python libraries.
- Loaded the telecom dataset using Pandas.
- Examined dataset information, structure, and initial records.
- Checked the original dataset dimensions.

### 2. Data Cleaning
- Identified missing values in different columns.
- Removed exact duplicate records.
- Removed the unnecessary duplicate column `monthly_data_mb_dup`.
- Converted `monthly_minutes` into a numeric data type.
- Standardized categorical values by removing whitespace and converting text to lowercase.

### 3. Missing Value Handling
Applied different techniques to handle missing values:

- Mean imputation for `monthly_data_mb`.
- Median imputation for `monthly_minutes` and `monthly_sms`.
- Mean-based imputation for `contract_months`.
- Mode imputation for `overdue_payments`.
- Mode-based imputation for categorical features.
- Removed records where the target variable `churn_next_month` was missing.

### 4. Handling Inconsistent Data

Corrected spelling mistakes and inconsistent categorical values.

Examples:

- `y`, `ye`, `ys` → `yes`
- `n`, `o` → `no`
- `basc`, `baic`, `basi` → `basic`
- `sandard` → `standard`
- Different misspellings of `unlimited` → `unlimited`

This helped maintain consistency in categorical features.

### 5. Categorical Encoding

Used **One-Hot Encoding** with `pandas.get_dummies()` to convert categorical variables:

- `plan_type`
- `has_family_plan`

Also removed the unnecessary `user_id` column from the encoded dataset.

### 6. Feature Scaling

Used Scikit-learn's `StandardScaler` to standardize numerical features:

- `monthly_minutes`
- `monthly_data_mb`
- `monthly_sms`
- `contract_months`
- `overdue_payments`

This transforms numerical features to a common scale.

### 7. Outlier Handling

Used the **Interquartile Range (IQR) method** to detect and handle outliers in numerical features.

The IQR method uses:

- Q1 (First Quartile)
- Q3 (Third Quartile)
- IQR = Q3 − Q1

Outlier boundaries:

- Lower Bound = Q1 − 1.5 × IQR
- Upper Bound = Q3 + 1.5 × IQR

Values outside these boundaries were capped using the corresponding lower and upper bounds.

## 📈 Exploratory Data Analysis (EDA)

Performed three types of analysis:

### A. Univariate Analysis

Analyzed individual variables using:

- Bar Chart – Distribution of telecom plan types.
- Count Plot – Number of customers in each plan category.
- Pie Chart – Customer churn ratio.
- Histogram – Distribution of monthly minutes usage.
- Violin Plot – Distribution of contract duration.

### B. Bivariate Analysis

Explored relationships between two variables using:

- Scatter Plot – Monthly minutes vs monthly data usage.
- Grouped Count Plot – Plan type vs churn status.
- Stacked Bar Chart – Family plan vs churn proportion.
- Box Plot – Contract duration vs churn status.

### C. Multivariate Analysis

Explored relationships among multiple variables using:

- Correlation Heatmap – Correlation between numerical and encoded features.
- Pair Plot – Relationships between numerical features based on churn status.

## 📁 Output

The notebook exports a preprocessed dataset named:

`telecom_churn_preprocessed.csv`

This dataset contains cleaned and encoded features and can be used as input for further analysis or machine learning experiments.

## 🚀 How to Run This Project

**Step 1:** Clone the repository.

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

**Step 2:** Navigate to the project directory.

```bash
cd Telecom-Customer-Churn-EDA
```

**Step 3:** Install the required libraries.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

**Step 4:** Open the notebook using Jupyter Notebook or Google Colab.

**Step 5:** Upload `telecom_usage_mixed.csv` and update the dataset path if necessary.

**Step 6:** Run all notebook cells to perform preprocessing and exploratory data analysis.

## 💡 Key Learning Outcomes

Through this project, I gained practical experience in:

- Working with real-world datasets.
- Data cleaning and preprocessing techniques.
- Handling missing and duplicate values.
- Categorical data encoding.
- Feature scaling and outlier treatment.
- Univariate, bivariate, and multivariate analysis.
- Creating meaningful visualizations using Python.
- Using GitHub to manage and showcase data analysis projects.

## 🔮 Future Improvements

- Build a Machine Learning model to predict customer churn.
- Compare classification algorithms such as Logistic Regression, Decision Tree, and Random Forest.
- Evaluate model performance using accuracy, precision, recall, and F1-score.
- Identify the most important factors influencing customer churn.

## 👩‍💻 Author

**Hema Latha**



---

⭐ If you find this project useful, feel free to explore the notebook and share your feedback!
