📊 Marketing Campaign Analysis — A/B Testing Project

An end-to-end data analytics and statistical testing project comparing two digital advertising campaigns — Facebook Ads vs Google AdWords — using a full year of daily performance data (365 days, 2019).

The goal is to determine which platform delivers better conversions, ROI, and cost-effectiveness, and to provide actionable recommendations to optimize marketing spend.

📝 Project Overview

Marketing teams often run parallel ad campaigns across different platforms. However, determining which platform performs better requires statistical evidence, not assumptions.

This project performs:

A/B Testing (Hypothesis Testing)

Correlation Analysis

Linear Regression Modeling

Cost-Per-Conversion & CPC Trend Analysis

Weekly & Monthly Seasonality Analysis

Cointegration Testing (Long-term Spend ↔ Conversion Relationship)

Everything is executed programmatically using Python, and insights are communicated visually through structured plots and summary tables.

🚀 Key Objectives

Compare the effectiveness of Facebook Ads vs AdWords on:

Clicks

Conversions

Cost-per-Click (CPC)

Cost-per-Conversion (CPCon)

Overall ROI

Identify statistically superior platform using:

A/B hypothesis testing

Mean comparison

P-value significance testing

Build predictive regression models to understand:

Relationship between clicks and conversions

Expected conversions for different click volumes

Analyze time-based patterns:

Weekly trends (which weekdays convert best?)

Monthly patterns (which months under/overperform?)

Seasonal drop zones

Provide data-backed marketing strategy recommendations.

🛠️ Tools & Technologies

{{[ Python }{\textbar}{ Pandas }{\textbar}{ Seaborn }{\textbar}{ Matplotlib }{\textbar}{ Scikit-learn }{\textbar}{ Statsmodels ]}}{}

Additional tools:

Jupyter Notebook

CSV data source

Numpy

📂 Project Structure
📁 Marketing-Campaign-AB-Testing
│
├── data/
│   └── marketing_campaign_2019.csv
│
├── notebook/
│   └── AB Testing (Marketing Campaigns).ipynb
│
├── images/
│   ├── conversion_trends.png
│   ├── regression_plot.png
│   ├── weekly_trends.png
│   └── cpc_comparison.png
│
└── README.md

📊 Data Description

The dataset includes 365 daily observations for both platforms, with columns:

date

views

clicks

conversions

cost

ctr – click-through rate

conversion_rate

cost_per_click

Additional engineered fields: month, weekday, CPC trends

🔍 Analysis Workflow
1️⃣ Data Cleaning & Preprocessing

Converted date column to datetime

Removed % and $ symbols

Converted numeric columns to floats

Extracted month and weekday

Verified missing values & dtypes

2️⃣ Exploratory Data Analysis (EDA)

Distribution plots (KDE + histograms) for clicks and conversions

Identification of high/low conversion intervals

Side-by-side comparison of daily conversion categories (Facebook vs AdWords)

Scatter plots of clicks vs conversions

3️⃣ Correlation Analysis

Computed Pearson correlation coefficients:

Facebook clicks ↔ conversions

AdWords clicks ↔ conversions

Used scatter plots + regression lines to visualize linearity.

4️⃣ A/B Testing (Hypothesis Testing)

Hypotheses:

H₀ (Null): Mean conversions (Facebook) = Mean conversions (AdWords)

H₁ (Alternate): Mean conversions differ

Method: Two-sample t-test

📌 Result:

p-value < 0.05 → Reject H₀

Facebook produced significantly more conversions.

5️⃣ Regression Modeling

Built linear regression model using:

X = clicks

y = conversions

Evaluation:

R² ≈ 0.76

MSE ≈ 2.02

Predictions:

~13 conversions for 50 clicks

~19 conversions for 80 clicks

6️⃣ Time Series & Seasonality Analysis
📅 Weekly Trends

Monday & Tuesday have the highest conversions

Weekends are comparatively stable but slightly lower

🗓️ Monthly Trends

Months with major drops:

February

April

August

November

Overall yearly trend = upward trajectory in conversions.

7️⃣ Cost Per Conversion Analysis

Identified low-CPCon months (high cost efficiency)

Highlighted months requiring budget optimization

8️⃣ Cointegration Testing (Long-Term Relationship)

Tested whether cost and conversions move together long-term.

📌 Result:

p-value < 0.05 → Long-term equilibrium exists

This helps in sustainable budget planning and ROI optimization.

🧠 Insights & Recommendations

Based on analyses:

Facebook outperforms AdWords across conversions, CPC, and cost-efficiency.

Allocate higher budget to Facebook campaigns.

Run aggressive campaigns on Mondays & Tuesdays (highest conversion days).

Shift spend to months with historically lower CPC.

Re-evaluate strategy during low-performing months (Feb, Apr, Aug, Nov).

Use regression predictions for conversion forecasting and KPI planning.

🏁 Conclusion

This project demonstrates how a Data Analyst can use:

A/B testing

Statistical hypothesis testing

Regression modeling

Time-series insights

Business metric evaluation

To drive data-backed decisions in digital marketing.
