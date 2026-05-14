# 📊 End-to-End HR Analytics & Attrition Power-BI/Tableau Project

## 📌 Project Executive Summary
This project addresses a critical business challenge: **Employee Attrition**. By combining Python's computational power for data engineering with Tableau’s visual storytelling, I transformed a raw dataset of 39 parameters into a strategic tool for HR decision-making. 

The analysis identifies high-risk departments, evaluates the financial impact of turnover, and correlates workplace environment factors with employee retention.

---

## 🛠️ The Technical Workflow

### 1. Data Engineering & EDA (Jupyter Notebook)
Before any visualization, the data underwent a rigorous audit in a Python environment to ensure "Single Version of Truth" (SVOT).
*   **Integrity Audit:** Verified that the dataset had zero missing values across all 1,470+ rows and 39 columns.
*   **Feature Engineering:** 
    *   Developed custom logic for `CF_age band` to group employees into demographic clusters.
    *   Standardized the `Attrition` column into a binary label (`CF_attrition label`) for cleaner aggregation.
*   **Exploratory Data Analysis (EDA):** 
    *   Used **Seaborn** and **Matplotlib** to identify initial correlations between `Monthly Income` and `Attrition`.
    *   Discovered that `Overtime` was a leading indicator of churn, which guided the dashboard's design focus.

### 2. Dashboard Architecture (Tableau/Power BI)
The cleaned data was exported to a `.csv` format and imported into the visualization tool to build an interactive ecosystem.
*   **KPI Tracking:** Created dynamic cards for **Attrition Rate**, **Active Employee Count**, and **Average Age**.
*   **Visual Logic:** 
    *   **Donut Charts:** Used for Department-wise distribution to provide a quick "share of total" view.
    *   **Histograms:** Implemented for Age Band analysis to visualize the "Attrition Peak" in younger demographics.
    *   **Cross-tab Matrix:** Designed to map Job Satisfaction vs. Job Roles, highlighting specific "Red Zones" within the organization.

---

## 📂 Project Repository Structure
```text
|-- hr-analytics-solution/
    |-- notebooks/
        |-- Untitled17.ipynb          # Full Python source code for Cleaning & EDA
    |-- data/
        |-- HR_Data_Raw.xlsx          # Original source file
        |-- HR_Cleaned_Final.csv      # Processed data ready for Dashboarding
    |-- dashboard/
        |-- HR_Analytics_Final.twbx   # Interactive Tableau Workbook
    |-- assets/
        |-- dashboard_preview.png     # Visual screenshot of the final UI
    |-- README.md
