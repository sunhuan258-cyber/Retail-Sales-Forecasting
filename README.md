# Walmart Retail Sales Forecasting

**Author:** Captain Xiaohuan
**Date:** 2025-08-02

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 1. Project Overview

This project is an end-to-end data science initiative to forecast weekly sales for Walmart stores and departments. Utilizing historical sales data, the project implements a robust machine learning pipeline, including data cleaning, advanced feature engineering, and a comparative analysis of various models (SARIMAX, Prophet, and LightGBM).

The final deliverable is a comprehensive, multi-chapter Tableau story dashboard. This dashboard not only demonstrates the model's strong predictive performance on unseen data (the entire 2012 test set) but also translates technical insights into actionable business intelligence, showcasing a complete data-to-decision workflow.

---

## 2. Key Findings & Visualization Story

An interactive Tableau story was created to present the project's findings in a clear, structured, and professional manner.

### Chapter 1: Model Performance on Unseen Data
![Chapter 1: Overview](images/01_overview.png)
*   **Key Insight:** This chapter showcases the model's remarkable performance on the 2012 test set. Trained solely on 2010-2011 data, the model's predictions (orange line) closely track the actual sales (blue line), proving its strong generalization capabilities.

### Chapter 2: Peak Sales Analysis (Stress Test)
![Chapter 2: Peak 1 Analysis](images/02_overview.png)
*   **Key Insight:** Focusing on the spring sales peak around April 6, 2012, we observed that the model successfully captured the upward trend but exhibited a two-week lag in predicting the exact peak. This highlights a key model characteristic and area for future improvement.

### Chapter 3: Stability Analysis (Cross-Validation)
![Chapter 3: Peak 2 Analysis](images/03_overview.png)
*   **Key Insight:** During the stable, non-peak period in July 2012, the model's forecast accurately captured the baseline trend while effectively filtering out random noise. This demonstrates its strength as a trend predictor rather than a noise follower.

### Chapter 4: From Prediction to Business Insight
![Chapter 4: Business Value](images/04_overview.png)
*   **Key Insight:** The final chapter translates the model's technical success into tangible business value, outlining its applications in intelligent inventory management, targeted marketing, and agile workforce allocation.

---

## 3. Modeling Process

- **Algorithm:** **LightGBM** was selected for its high efficiency and accuracy in handling large-scale tabular data.
- **Feature Engineering:** Key features included time-based attributes (year, month, week), lag features (sales from the previous week and year), and rolling-window features (e.g., 4-week rolling average).
- **Train/Test Strategy:** A strict temporal split was enforced using `2012-01-01` as the cutoff date, ensuring a realistic evaluation of the model's ability to forecast the future.

---

## 4. Technologies & Tools

- **Language:** Python
- **Libraries:** Pandas, Scikit-learn, LightGBM, Matplotlib, Seaborn, Prophet, Statsmodels
- **BI Tool:** Tableau
- **Version Control:** Git & GitHub

---

## 5. Getting Started

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/YourUsername/Retail-Sales-Forecasting.git
    ```
    (Please replace `YourUsername` with your actual GitHub username).
2.  **Explore the analysis:**
    - Raw data is located in the `/data` directory.
    - The complete analysis, feature engineering, and modeling process can be found in `/notebooks/walmart_sales_analysis.ipynb`.
3.  **Interact with the dashboard:**
    - Download the `walmart_sales_story.twbx` file from the root directory.
    - Open it with Tableau Public or Tableau Reader (free) to explore the interactive story.

---

## 6. Repository Structure

```
.
├── data/
├── images/
├── models/
├── notebooks/
├── .gitignore
├── LICENSE
├── README.md
└── walmart_sales_story.twbx
```