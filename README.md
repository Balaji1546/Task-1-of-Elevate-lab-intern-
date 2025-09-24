# 🧹 Marketing Campaign — Data Cleaning & Preprocessing

This repository contains a Python cleaning pipeline for the **Marketing Campaign** dataset (customer purchases & campaign responses).

## What the script does
- Loads dataset from `data/marketing_campaign.csv` or `data/marketing_campaign.xlsx`
- Cleans Excel artifacts (e.g., `#REF!`, `#N/A`)
- Normalizes column names to `lowercase_with_underscores`
- Parses mixed-format dates (e.g., `dt_customer`) using `dateutil`
- Cleans `income` robustly and fills missing values with **median**
- Cleans `kidhome` / `teenhome` (handles `#REF!`)
- Creates `age` from `year_birth`
- Computes `total_spent` (sum of all `mnt*` columns)
- Computes `total_num_purchases` (sum of all `num*` columns)
- Converts boolean/binary columns (AcceptedCmp*, Complain, Response) to integers
- Removes duplicates and saves cleaned CSV/XLSX to `cleaned/`

## Files
- `marketing_campaign_cleaning.py` — main cleaning script
- `data/marketing_campaign.csv` — original dataset (CSV or Excel)
- `cleaned/marketing_campaign_cleaned.csv` — cleaned output

## Requirements
```bash
pip install pandas openpyxl python-dateutil
