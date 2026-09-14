# Banking Customer EDA & Dashboard

An end-to-end banking customer analysis project — from raw data to an interactive Power BI dashboard.

This project explores banking customer data to uncover insights around deposits, loans, risk profiles, and client segmentation. It covers the full workflow: merging multiple raw datasets, cleaning and exploring the data using Python, and building an interactive 3-page Power BI dashboard.

## 📊 Project Overview

- **Domain:** Banking / Financial Services
- **Goal:** Understand customer behavior, financial holdings, and risk profiles to support data-driven business decisions
- **Dataset size:** ~3,000 customers, 4 source tables

## 🗂️ Dataset

The raw data consists of 4 CSV files (found in `/data`):

| File | Description |
|---|---|
| `banking-clients.csv` | Main client table — demographics, income, deposits, loans, etc. |
| `banking-relationships.csv` | Lookup table mapping Banking Relationship IDs to types (Retail, Institutional, etc.) |
| `gender.csv` | Lookup table mapping Gender IDs to labels |
| `investment-advisiors.csv` | Lookup table mapping Investment Advisor IDs to names |

These were merged into a single clean dataset (`banking_merged.csv`) using Python/Pandas before analysis.

## 🧹 Data Cleaning

- Merged 4 tables into one unified dataset using `pandas.merge()`
- Fixed duplicate Client IDs (same ID assigned to different customers)
- Converted `Joined Bank` to a proper datetime type
- Checked for missing values and outliers
- Created an `Income Band` feature (Low / Mid / High) using `pd.cut()`

## 🔍 Exploratory Data Analysis (Python)

Performed in Jupyter Notebook using **Pandas**, **Matplotlib**, and **Seaborn**:

- Univariate analysis of key demographic and financial columns
- Bivariate analysis (e.g. Occupation vs Income, Gender vs Loyalty Classification)
- Correlation heatmap across financial variables (deposits, savings, loans, credit cards)
- Regression plots exploring relationships like Age vs Superannuation Savings

**Key insight:** Bank Deposits show strong correlation with Saving and Checking Accounts, suggesting overlapping saver behavior across product types — an opportunity for cross-selling.

## 📈 Power BI Dashboard

An interactive 3-page dashboard built on the cleaned dataset:

### Page 1 — Executive Overview
KPI cards (Total Clients, Deposits, Loans, Avg Income), deposit & loan trends over time, relationship breakdown, and income band analysis.

### Page 2 — Client Portfolio & Segmentation
Income by occupation, deposit distribution by gender & loyalty tier, income vs checking balance scatter plot, and a detailed client directory.

### Page 3 — Risk & Product Analytics
Risk weighting distribution, loan breakdown by relationship type, investment advisor performance, and risk-based financial metrics.

## 🛠️ Tools Used

- **Python** (Pandas, NumPy, Matplotlib, Seaborn) — data cleaning & EDA
- **Jupyter Notebook** — analysis environment
- **Power BI Desktop** — dashboard & visualization

## 📁 Repository Structure
