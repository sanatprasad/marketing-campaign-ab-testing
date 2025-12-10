
---

# 📊 Marketing Campaign Analysis — A/B Testing & Regression Project

**Tools:** Python • Pandas • NumPy • Seaborn • Matplotlib • Scikit-learn • Statsmodels

---

## 📁 Project Repository

**Suggested Repo Name:**
👉 `marketing-campaign-ab-testing-analysis`

---

## 📝 Project Overview

This project performs a full **Marketing Campaign Analysis** comparing **Facebook Ads** and **Google AdWords** using **A/B Testing**, **Statistical Analysis**, **Regression Modeling**, and **Time-Series Insights**.

Using **365 days of campaign performance data**, the goal is to identify which advertising platform delivers:

* Higher **clicks**
* Better **conversion rates**
* Lower **cost per conversion (CPC)**
* Stronger **ROI**
* More stable long-term performance

The project simulates the work of a **Data Analyst in a marketing agency**, where data-driven insights directly influence ad-spend decisions and campaign optimization strategies.

---

## 🎯 Business Objective

> **Maximize Return on Investment (ROI)** for ad campaigns by identifying the more effective platform between Facebook and AdWords, based on conversions, clicks, engagement, and cost-effectiveness.

---

## 📂 Dataset Description

The dataset contains **daily campaign data for 2019** (Jan 1 – Dec 31), including:

| Column          | Description                    |
| --------------- | ------------------------------ |
| Date            | Daily timestamp                |
| Views           | Number of ad impressions       |
| Clicks          | Number of user clicks          |
| Conversions     | Desired actions taken by users |
| Cost            | Daily advertising spend        |
| CTR             | Click-Through Rate             |
| Conversion Rate | Conversions / Clicks           |
| CPC             | Cost per Click                 |
| CPConversion    | Cost per Conversion            |

Datasets exist for **both platforms**, enabling direct comparison.

---

# 🛠️ Tools & Technologies Used

* **Python**
* **Pandas** – Data cleaning & preparation
* **NumPy** – Numerical operations
* **Matplotlib & Seaborn** – Data visualization
* **Scikit-learn** – Linear Regression, Model Evaluation (R², MSE)
* **Statsmodels** – A/B testing (T-test), Cointegration Test
* **Jupyter Notebook** – Full analysis workflow

---

# 📈 Steps Performed in the Project

## **1️⃣ Data Cleaning & Preprocessing**

* Loaded CSV data for both campaigns
* Converted `date` column to datetime
* Removed `%` and `$` symbols from numeric columns
* Converted all metrics to appropriate numeric types
* Created additional time-based features:

  * Month
  * Weekday
  * Week number

---

## **2️⃣ Exploratory Data Analysis (EDA)**

* Summary statistics for clicks, conversions, cost
* Histograms & KDE plots for distribution analysis
* Identified high-conversion days and buckets (<6, 6-10, 10-15, >15 conversions)
* Side-by-side bar charts comparing platform performance

---

## **3️⃣ Correlation Analysis**

* Scatter plots of **Clicks vs Conversions**
* Positive correlations were observed
* Relationships varied across platforms
* Facebook showed a stronger click → conversion path

---

## **4️⃣ A/B Testing (Hypothesis Testing)**

Performed a **two-sample T-test** comparing mean conversions:

* **Null Hypothesis (H₀):** No difference between Facebook & AdWords
* **Alternative Hypothesis (H₁):** Facebook conversions > AdWords conversions

**Result:**

* p-value < significance level
* **Reject H₀ → Facebook ads significantly outperform AdWords**

---

## **5️⃣ Regression Modeling**

Using Scikit-learn’s **Linear Regression**:

* X = Clicks
* y = Conversions
* Model trained on daily data

### 📊 Model Evaluation:

* **R² ≈ 0.76** — Strong predictive power
* **MSE ≈ 2.02**

### 🔮 Predictions:

* ~50 clicks → ~13 conversions
* ~80 clicks → ~19 conversions

This model helps estimate conversions based on expected traffic.

---

## **6️⃣ Time-Series & Trend Analysis**

### Weekly Insights

* Mondays & Tuesdays show **highest conversions**
* Weekends show moderate, consistent performance

### Monthly Insights

* Significant dips observed in:
  **February, April, June, August, November**
* Overall yearly trend → **Upward movement**

---

## **7️⃣ Cost & CPC Analysis**

* Monthly **Cost per Conversion (CPConversion)** tracked
* Months with lowest CPC → **May & November**
* Higher CPC → Lower campaign efficiency
* Recommended budget shifts to months with better historical ROI

---

## **8️⃣ Cointegration Test (Long-Term Relationship)**

Tested whether **ad spend** and **conversions** have a stable long-term equilibrium.

**Result:**

* p-value < critical value
* **Long-term equilibrium exists**

> Meaning: Increasing spend → reliably increases conversions over time.

---

# 🧠 Key Insights & Business Recommendations

### ✔ Facebook is statistically **more effective** than AdWords

(T-test + higher conversion buckets)

### ✔ Increase spend on months with historically low CPC

(May, November)

### ✔ Focus campaign pushes early in the week

(Monday & Tuesday perform best)

### ✔ Regression model can predict conversions based on clicks

(Useful for forecasting)

### ✔ Strong long-term relationship between spend & conversions

(Helps in annual budget planning)

---

# 📊 Visualizations Included

* Histograms
* KDE distributions
* Scatter plots
* Weekly/Monthly trend charts
* Side-by-side bar charts
* Regression line plots
* CPC trend lines

---

# 🚀 Project Deliverables

* Cleaned dataset
* Jupyter Notebook with full analysis
* Visual dashboards & charts
* Statistical test outputs (T-Test, correlation, cointegration)
* Regression predictions and model evaluation
* Detailed insights & recommendations

---

# 📘 How to Run the Project

```bash
pip install -r requirements.txt
jupyter notebook
```

Open the file:

```
AB Testing (Marketing Campaigns).ipynb
```

---

# 📧 Contact

For suggestions or improvements, feel free to open an issue or contribute!

---

If you want, I can also generate:
✅ A **GitHub repo structure**
✅ A **requirements.txt**
✅ A **cover image for the project**
Just tell me!
