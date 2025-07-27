# Name: SADE George Sade
# ID: 
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
- Performed data type corrections
- Feature engineering:
  - Extracted `hour`, `day`, `month`, `day_of_week` from `pickup_datetime`
  - Created `is_peak` flag for peak hour categorization
- Saved clean data as `uber_enhanced.csv`

---

### 2. 📊 Exploratory Data Analysis (Python & Power BI)
- Descriptive statistics: mean, median, quartiles
- Visuals created:
  - Histogram & box plot of fare amounts
  - Line chart of monthly trends
  - Matrix heatmap of hourly/weekday fares
  - Bar charts for fares by hour/day
  - KPI cards for total rides, average fare, etc.
  - Map of ride pickups (if coordinates available)

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
| `Assignment_Report.pptx` | Final report (PowerPoint format or GitHub markdown) |

---

## 📸 Screenshots (in `/screenshots/`)
- 📂 Data loading and cleaning process
- 🧮 Feature engineering steps
- 📊 Power BI visualizations & dashboard
- ⚙️ DAX measures (if used)

---

## 🧾 Final Report

You may choose one of the two:
- 📘 GitHub-style Markdown report (`README.md`)
- 📽️ PowerPoint presentation with slides on:
  - Dataset overview
  - Data preparation & tools
  - Dashboard walkthrough
  - Key results & recommendations

---

## ✅ Recommendations

💡 Uber can:
- Allocate more drivers during peak hours
- Introduce dynamic pricing based on hour and day of week
- Analyze demand clusters using geographic data
- Offer time-based discounts during low-demand periods

---

## 📬 Submission

- ✅ Public GitHub repository created
- ✅ All files & documentation uploaded
- ✅ Email sent to **eric.maniraguha@auca.ac.rw** with GitHub repo link
- ✅ Deadline respected (before Sabbath on 25 July 2025)

---

## 🛡️ Academic Integrity Notice

All analysis, visualizations, and documentation are
