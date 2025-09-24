# 🧹 Sample Superstore — Data Cleaning & Preprocessing

This repository contains Python code to clean and preprocess the popular **Sample Superstore** dataset.  
It supports inputs in **CSV** or **Excel** formats and demonstrates best practices for data cleaning using **pandas**.

## 🚀 What This Script Does
- Loads dataset from `data/SampleSuperstore.csv`
- Identifies and handles missing values (fills numeric with **median**, categorical with **mode**)
- Removes duplicate rows using `drop_duplicates()`
- Cleans Excel artifacts (e.g., `#REF!`, `NA`, stray characters)
- Standardizes text values (segment, region, category, sub-category)
- Converts date columns (e.g., `dt_customer`) to `datetime`, handling mixed formats using `dateutil`
- Creates `age` column from `year_birth` (exact if `date_of_birth` exists, otherwise approximate)
- Renames columns to lowercase with underscores for consistency
- Saves cleaned data to both CSV and Excel in `cleaned/`

## 📂 Files
- `superstore_cleaning.py` — main cleaning script
- `data/SampleSuperstore.csv` or `data/SampleSuperstore.xlsx` — original dataset
- `cleaned/superstore_cleaned.csv` — cleaned output (generated)
- `cleaned/superstore_cleaned.xlsx` — cleaned output (generated)
- `notebooks/` — optional Jupyter notebooks for further analysis or visualization
- `images/` — screenshots of dashboards

## 🛠️ Requirements
```bash
pip install pandas openpyxl python-dateutil
