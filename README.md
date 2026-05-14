# Titanic Missing Value Imputation Analysis

## 🚀 Project Overview
This project focuses on handling missing values in the **Titanic Dataset** using multiple imputation techniques and evaluating their effectiveness using **Root Mean Squared Error (RMSE)**. The objective is to compare different preprocessing strategies and determine which method provides the most accurate estimation for missing `Age` values.

The project implements and evaluates:

- ✅ Mean Imputation  
- ✅ Median Imputation  
- ✅ K-Nearest Neighbors (KNN) Imputation  

A validation strategy was created by masking a portion of known `Age` values and comparing the imputed results against the original values.

---

## 📌 Problem Statement
Missing values are one of the most common challenges in real-world datasets. This project analyzes missing values in the `Age` column of the Titanic dataset and compares different imputation methods to identify the best-performing technique.

The performance of each method is evaluated using:

- 📊 Root Mean Squared Error (RMSE)

---

## 📂 Dataset

Dataset Used: **Titanic Dataset**

- Kaggle Dataset:  
  https://www.kaggle.com/competitions/titanic/data

- Direct CSV Source:  
  https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

---

## 🔥 Key Features

- ✅ Missing value analysis and visualization
- ✅ Mean and Median statistical imputation
- ✅ KNN-based imputation using related features
- ✅ RMSE evaluation for model comparison
- ✅ Exploratory Data Analysis (EDA)
- ✅ Power BI Dashboard visualization
- ✅ Comparison of imputation techniques

---

## 📊 Exploratory Data Analysis

The dataset was analyzed to identify:

- Total missing values
- Percentage of missing values
- Distribution of the `Age` column
- Passenger class distribution
- Survival distribution

Dashboard insights include:

- Passenger survival distribution
- Passenger age distribution
- Passenger class distribution
- RMSE comparison between imputation methods

---

## ⚙️ Imputation Techniques Used

### 1️⃣ Mean Imputation
Replaces missing `Age` values using the mean age of all passengers.

### 2️⃣ Median Imputation
Replaces missing `Age` values using the median age.

### 3️⃣ KNN Imputation
Uses neighboring samples and related features such as:

- `Fare`
- `Pclass`
- `SibSp`
- `Parch`

to estimate missing values more accurately.

Implemented using:

```python
from sklearn.impute import KNNImputer
```

---

## 📊 Validation Strategy

To properly evaluate imputation quality:

1. Rows with existing `Age` values were selected.
2. Randomly masked 20% of the `Age` values.
3. Hidden values were treated as ground truth.
4. Imputed values were compared against original values.

---

## 📈 RMSE Comparison

| Imputation Method | RMSE |
|-------------------|------|
| Mean Imputation   | Higher RMSE |
| Median Imputation | Higher RMSE |
| KNN Imputation    | Lowest RMSE ✅ |

### 📌 Observation
KNN Imputation performed better because it considers relationships between multiple features rather than relying on a single statistical measure.

---

## 📊 Dashboard Insights

The Power BI dashboard includes:

- Passenger survival distribution
- Total passengers count
- Passenger class distribution
- Passenger age histogram
- RMSE comparison chart

---

## 🧠 Technical Workflow

| Step | Description |
|------|-------------|
| Data Loading | Imported Titanic dataset using Pandas |
| Missing Value Analysis | Identified null values and percentages |
| Validation Strategy | Random masking of Age values |
| Mean Imputation | Statistical replacement using mean |
| Median Imputation | Statistical replacement using median |
| KNN Imputation | Feature-based nearest neighbor estimation |
| RMSE Evaluation | Compared imputed values with ground truth |
| Visualization | Created plots and Power BI dashboard |

---

## 🛠 Technologies Used

- 🔹 Python
- 🔹 Pandas
- 🔹 NumPy
- 🔹 Scikit-learn
- 🔹 Matplotlib
- 🔹 Seaborn
- 🔹 Power BI
- 🔹 Jupyter Notebook

---

## 🚀 Installation & Setup

### 🔹 Clone the Repository

```bash
git clone https://github.com/your-username/titanic-missing-value-imputation.git

cd titanic-missing-value-imputation
```

### 🔹 Install Dependencies

```bash
pip install -r requirements.txt
```

### 🔹 Run the Notebook

```bash
jupyter notebook
```

Open:

```bash
KNN (1)(1).ipynb
```

---

## 📊 Results

- ✅ KNN Imputation achieved the best performance
- ✅ Improved estimation accuracy compared to statistical methods
- ✅ RMSE-based evaluation ensured objective comparison
- ✅ Dashboard provided clear visual insights

---

## 🔮 Future Improvements

- 🔹 Experiment with different K values
- 🔹 Compare advanced imputation techniques
- 🔹 Use deep learning-based imputation models
- 🔹 Deploy dashboard as an interactive web app

---

## 📬 Contributions

Contributions are welcome! Feel free to fork this repository and submit pull requests.

---

## 📧 Contact

For queries or collaboration:

- **Author:** Rishi Anand

---

🌟 **Give this project a star if you found it useful!** ⭐
