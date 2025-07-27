# Name: SADE George Sade
# ID:  26915
# 🚕 Uber Fares Data Analysis Project — Power BI

📊 **Course**: Introduction to Big Data Analytics (INSY 8413)  
👨‍🏫 **Instructor**: Eric Maniraguha | eric.maniraguha@auca.ac.rw  
📅 **Assignment Date**: 20 July 2025  
📁 **Groups**: B   

---

## 🎯 Objective

The goal of this project is to analyze the **Uber Fares Dataset** to gain meaningful insights into fare amounts, ride patterns, time-based behaviors, and location-based trends. The final output includes a **fully interactive Power BI dashboard** and a detailed report documenting methodology and results.

---

## 🛠️ Tools & Technologies

- 🐍 **Python (Pandas, Seaborn)** — for data cleaning & preprocessing  
- 📈 **Power BI Desktop** — for visualization & dashboard creation  
- 🗃️ **GitHub** — for version control and submission  

---

## 📦 Dataset

📌 Source: [Uber Fares Dataset – Kaggle](https://www.kaggle.com/datasets/yasserh/uber-fares-dataset)  
🧾 Description: Includes trip data such as fare amounts, pickup time, pickup/dropoff coordinates.

---

## 🔍 Process Overview

### 1. 📥 Data Preparation (Python)
- Loaded raw dataset using
  ```python
     import pandas as pd

     # Replace 'uber.csv' if the name is different (check output from Step 1)
     df = pd.read_csv("uber.csv")
         print("✅ Dataset loaded successfully!")
         df.head()
  ```
- Checked and removed missing/null values
  ```Python
    # Basic Info
     print(f"Rows: {df.shape[0]}, Columns: {df.shape[1]}")
     print("\nColumn types:\n", df.dtypes)

     # Check missing values
     print("\nMissing values:\n", df.isnull().sum())

     # Drop missing
     df_cleaned = df.dropna()
     print("\nAfter cleaning:\n", df_cleaned.isnull().sum())
     df_cleaned.shape
  ```
- Performed data type corrections
- Feature engineering:
  ```Python
  df_cleaned['pickup_datetime'] = pd.to_datetime(df_cleaned['pickup_datetime'])
  df_cleaned['hour'] = df_cleaned['pickup_datetime'].dt.hour
  df_cleaned['day'] = df_cleaned['pickup_datetime'].dt.day
  df_cleaned['month'] = df_cleaned['pickup_datetime'].dt.month
  df_cleaned['day_of_week'] = df_cleaned['pickup_datetime'].dt.day_name()
  df_cleaned['is_peak'] = df_cleaned['hour'].apply(lambda h: 1 if 7 <= h <= 9 or 17 <= h <= 19 else 0)

   df_cleaned.head()
  ```
  - Extracted `hour`, `day`, `month`, `day_of_week` from `pickup_datetime`
  - Created `is_peak` flag for peak hour categorization
- Saved clean data as `uber_enhanced.csv`
  ```Python
  df_cleaned.to_csv("uber_enhanced.csv", index=False)
  from google.colab import files
  files.download("uber_enhanced.csv")
  ```

---

### 2. 📊 Exploratory Data Analysis (Python & Power BI)
- Descriptive statistics: mean, median, quartiles
- Visuals created:
  - Histogram & box plot of fare amounts
 
     <img width="271" height="234" alt="Screenshot 2025-07-27 190836" src="https://github.com/user-attachments/assets/2d191342-86c5-4073-9cc9-33893b6fc347" />
     
  - Line chart of monthly trends
    
     <img width="286" height="235" alt="Screenshot 2025-07-27 192451" src="https://github.com/user-attachments/assets/75cc7831-31eb-49a8-a9d9-0e2aaf8fa443" />
     
  - Matrix heatmap of hourly/weekday fares

      <img width="377" height="286" alt="Screenshot 2025-07-27 192906" src="https://github.com/user-attachments/assets/467ee435-dcc3-4a81-bb18-05fd27d431ce" />

  - Bar charts for fares by hour/day

      <img width="307" height="234" alt="Screenshot 2025-07-27 193245" src="https://github.com/user-attachments/assets/94b35981-132a-442e-a17b-4918351ac24a" />

  - KPI cards for total rides, average fare, etc.
 
      <img width="514" height="331" alt="Screenshot 2025-07-27 193845" src="https://github.com/user-attachments/assets/6c74d0a3-de0f-4e89-aac5-9bbc8d231e12" />
   
  - Map of ride pickups (if coordinates available)
 
    <img width="748" height="313" alt="Screenshot 2025-07-27 194041" src="https://github.com/user-attachments/assets/33954d31-24c2-4ca1-ae6c-172720ede636" />


---

### 3. 🧠 Insights & Findings
- Peak hours (7–9 AM and 5–7 PM) have higher average fares
- Weekends show different ride patterns compared to weekdays
- Certain hours consistently show outliers in fare distribution
- Geographic clustering of pickups can help optimize driver allocation

---

## 📌 Deliverables

| File/Folder              | Description |
|--------------------------|-------------|
| `uber_enhanced.csv`      | Cleaned and engineered dataset |
| `uber_dashboard.pbix`    | Power BI dashboard file |
| `/screenshots/`          | Step-by-step process visuals |
| `README.md`              | Project documentation |

---

## 📸 Screenshots 
- 📂 Data loading and cleaning process

<img width="913" height="248" alt="load_data" src="https://github.com/user-attachments/assets/36bd6549-ef50-4e9b-b2d1-30768b85d681" />

<img width="331" height="335" alt="clean_missing_data" src="https://github.com/user-attachments/assets/46f04225-41f7-4cbd-8e4a-70c721166ec8" />

- 🧮 Feature engineering steps

  <img width="882" height="251" alt="feature_engineering" src="https://github.com/user-attachments/assets/39d90bb3-7fe1-4b91-88f3-62157d581958" />

- 📊 Power BI visualizations & dashboard

  <img width="659" height="372" alt="PowerBI_Visuals" src="https://github.com/user-attachments/assets/84bebf40-af15-4e3b-8d13-29a2163dbe1b" />

---
