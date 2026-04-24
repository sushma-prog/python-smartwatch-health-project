# 📊 Smartwatch Health Data Analysis

## 📌 Project Overview

This project focuses on analyzing a smartwatch health dataset containing user health and activity metrics. The goal is to clean the data, handle inconsistencies, and extract meaningful insights using data analysis and visualization techniques.

---

## 📂 Dataset Description

The dataset includes the following columns:

* **User ID** – Unique identifier for each user
* **Heart Rate (BPM)** – Heart rate of the user
* **Blood Oxygen Level (%)** – Oxygen level in blood
* **Step Count** – Number of steps taken
* **Sleep Duration (hours)** – Daily sleep duration
* **Stress Level** – Stress level of the user
* **Activity Level** – Category (sedentary, moderate, highly active)

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data cleaning and manipulation
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization

---

## 🔧 Data Cleaning Steps

### ✅ Handling Missing Values

* Filled numerical columns using **mean**
* Converted columns to numeric using:

  ```python
  pd.to_numeric(errors='coerce')
  ```
* Filled categorical column (**Activity Level**) using **mode**
* Removed rows with missing **User ID**

---

### ✅ Data Type Fixing

* Converted:

  * Sleep Duration → numeric
  * Stress Level → numeric

---

### ✅ Standardization

* Converted **Activity Level** to lowercase
* Removed extra spaces
* Fixed inconsistent values

---

### ✅ Outlier Removal

Filtered values using logical ranges:

* Heart Rate: **50 – 180 BPM**
* Blood Oxygen Level: **acceptable range**
* Removed unrealistic data points

---

### ✅ Duplicate Handling

* Checked for duplicate rows
* Displayed and analyzed duplicates

---

### ✅ Final Clean Dataset

* Saved cleaned data as:

  ```
  cleaned_smartwatch_health_data.csv
  ```

---

## 📊 Data Visualization

### 1. Heart Rate Distribution

* Histogram of heart rate values
* Shows most users fall in a healthy range

### 2. Activity Level Distribution

* Count plot of activity categories
* Majority users are sedentary

### 3. Sleep Duration vs Stress Level

* Scatter plot
* No strong relationship observed

### 4. Step Count Distribution

* Histogram showing step trends
* Right-skewed distribution

---

## 🔍 Key Observations

* Heart rate follows an **approximately normal distribution**
* Most users have **70–85 BPM**, indicating healthy range
* Majority users are **sedentary**
* Step count is **right-skewed** (most users < 8000 steps)
* No clear relationship between **sleep duration and stress level**

---

## 📌 Final Conclusion

* Dataset successfully cleaned and prepared for analysis
* Most users show **low activity levels**
* Health indicators are generally within normal ranges
* Lifestyle patterns suggest need for **more physical activity awareness**

---

## 🚀 Future Improvements

* Apply **machine learning models** for prediction
* Perform **correlation analysis**
* Build a **dashboard using Power BI / Tableau**
* Add **real-time health monitoring insights**

---

## 📁 Project Structure

```
├── smartwatch_health_data.ipynb
├── unclean_smartwatch_health_data.csv
├── cleaned_smartwatch_health_data.csv
└── README.md
```

---
