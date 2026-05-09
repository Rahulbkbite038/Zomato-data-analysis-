# 🍽️ Zomato Bangalore Restaurant Analysis & Rating Prediction

A complete data science project analyzing restaurant data from Zomato Bangalore.  
The project includes **data cleaning**, **exploratory data analysis (EDA)**, **predictive modeling** (regression & classification), and **customer segmentation (clustering)**.

---

## 📁 Dataset

- **Source**: Zomato Bangalore restaurants (CSV file)
- **Rows**: ~500 cleaned records
- **Features**: restaurant name, online ordering, table booking, rating, votes, location, cuisine type, cost for two, etc.

> ⚠️ The raw CSV contains malformed rows and embedded reviews. The script handles parsing robustly.

---

## 🎯 Project Goals

1. **Understand** which factors influence restaurant ratings.
2. **Build a regression model** to predict a restaurant's rating.
3. **Build a classification model** to categorize ratings (Low / Medium / High).
4. **Cluster restaurants** into segments for business insights.
5. **Provide actionable insights** for customers and restaurant owners.

---

## 🧰 Tools & Libraries

- Python 3.8+
- pandas, numpy – data manipulation
- matplotlib, seaborn – visualizations
- scikit-learn – preprocessing, modeling, clustering

---

## 📊 Key Steps

### 1. Data Cleaning
- Parsed CSV with `csv` module to handle quotes and multiline fields.
- Converted `rate` (e.g., "4.1/5") to numeric.
- Cleaned `cost` (removed commas, handled "NEW").
- Dropped rows with missing critical data.
- Created binary features: `online_order`, `book_table`.

### 2. Exploratory Data Analysis (EDA)
- Distribution of ratings and cost.
- Relationship between online ordering / table booking and rating.
- Top locations and cuisines by average rating.
- Correlation matrix of numeric features.

### 3. Feature Engineering
- Extracted `primary_cuisine` (first cuisine listed).
- Grouped rare locations and cuisines into "Other".
- Created target variable `rating_category` (Low, Medium, High).

### 4. Predictive Modeling
- **Regression** (Random Forest) – predict exact rating.
  - MAE, RMSE, R².
- **Classification** (Random Forest) – predict rating category.
  - Accuracy, Precision, Recall, F1-score.

### 5. Clustering (K‑Means)
- Used cost, votes, rating, online_order, book_table.
- Scaled features, determined optimal k via elbow method.
- Visualized clusters using PCA.
- Interpreted cluster characteristics.

---

## 📈 Results (Example Outputs)
