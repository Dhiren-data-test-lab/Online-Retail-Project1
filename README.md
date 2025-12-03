# Online Retail II — Project 1 (Sample Portfolio)

**Practice repository**: end-to-end analysis of the *Online Retail II* dataset (public, UCI).  
This repository contains a sample deliverable created for learning and portfolio purposes.

---

## 📌 Project Summary
- **Objective:** Demonstrate a full analytics pipeline — data loading, cleaning, validation, EDA, basic RFM segmentation, and reporting — suitable for a Data Analyst portfolio.
- **Dataset:** Online Retail II (public dataset) — combined Excel sheets for two fiscal years.
- **Deliverables (in this repo):**
  - `Online_Retail_Project_Summary_sample.pdf` — multi-page summary (charts + findings) — sample
  - `online_retail_cleaned_sample.csv` — cleaned sample dataset
  - `top_products.csv`, `country_revenue.csv`, `customer_revenue.csv` — aggregated outputs
  - `rfm_customers_sample.csv` — sample RFM results
  - `online_retail_project1.py` — main analysis pipeline (script)
  - `README.md` — this document

---

## ⚙️ How this project helps hiring managers
- Shows ability to work with large real-world transactional data.
- Demonstrates data cleaning choices and reasoning (handling cancellations, missing customer IDs, invalid prices/quantities).
- Contains visual summaries and a sample summary PDF — suitable to include in interviews.
- Provides a runnable `.py` script so clients/testers can reproduce results.

---

## 🧭 Quick Usage (run locally)
**Prerequisites:** Python 3.8+, and these packages:
```
pip install pandas numpy matplotlib openpyxl
```

**Run script (example):**
```bash
python online_retail_project1.py -i online_retail_II.xlsx -o or_outputs
```
- `-i` / `--input` : input Excel file (Online Retail II)
- `-o` / `--output` : output folder for CSVs and charts
- `--sheet` : optional, load a single sheet name
- `--dayfirst` : use if date format is DD/MM/YYYY
- `--no-charts` : skip saving chart PNGs

---

## 🧹 Cleaning choices (summary)
- Normalized column names (InvoiceNo, InvoiceDate, StockCode, Description, Quantity, UnitPrice, CustomerID, Country).
- Dropped unnamed / empty columns.
- Parsed `InvoiceDate` into `InvoiceDate_parsed`.
- Removed cancelled invoices (InvoiceNo starts with `C`).
- Dropped rows with missing `CustomerID` for customer-level analysis.
- Removed rows with non-positive `Quantity` or `UnitPrice`.
- Calculated `Revenue = Quantity * UnitPrice`.

> **Note:** All cleaning steps are conservative and explained in comments inside `online_retail_project1.py`. Adjust heuristics for final deliverable if you wish.

---

## 📊 Major outputs (sample)
- Top products (by revenue)
- Country-level revenue
- Customer revenue list (top customers)
- Monthly / weekly / daily revenue series
- Simple RFM segmentation (Recency, Frequency, Monetary)

Files with these outputs are included in the `/or_outputs` folder (or in the zip bundle provided).

---

## 📄 Project Summary PDF
`Online_Retail_Project_Summary_sample.pdf` contains:
- High-level numbers (rows processed, rows dropped)
- Top products and countries charts
- Monthly revenue chart
- Top customers and short RFM sample

> The PDF in this repo is a **sample** created from a sampled subset. Run the script locally on full dataset to regenerate the full report.

---

## ⚖️ Attribution & License
- Dataset source: **Online Retail II — UCI Machine Learning Repository** (public dataset). Use in portfolio with attribution.
- This repository content (code, report) is prepared for learning and portfolio purposes.
- You may reuse and adapt the `online_retail_project1.py` script for your own skill development.

---

## 📞 Contact / Next steps
- Full project suggestions: EDA expansion, cohort analysis, customer lifetime value (CLV), forecasting.
- This practice repository is the first part of a 3-project portfolio plan.

