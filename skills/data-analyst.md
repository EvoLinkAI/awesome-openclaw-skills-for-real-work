# Data Analyst

> Turn your agent into a data analyst — load datasets, generate insights, create charts, run SQL queries, and produce structured reports.

**ClawHub:** https://clawhub.ai/oyi77/data-analyst · ⭐ 51 · 183 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Data Analyst gives your agent a structured workflow for data analysis tasks. Load CSV/Excel datasets, clean data, run statistical analysis, create charts, query data with SQL, and produce clear, actionable reports. Perfect for small data tasks that don't require a full BI tool.

## How to Install

```bash
clawhub install data-analyst
```

## Key Capabilities

- Load CSV, Excel, JSON, and Parquet datasets
- Clean and transform data (handle nulls, normalize columns, filter)
- Run SQL queries against loaded datasets
- Generate charts (bar, line, pie, scatter, histogram)
- Compute descriptive statistics (mean, median, standard deviation, etc.)
- Identify trends, outliers, and correlations
- Produce structured reports with insights and recommendations
- Export results to CSV, JSON, or Markdown

## Usage Examples

**Load a dataset and get initial insights:**
```
"Load this sales.csv file and tell me the top 3 products by revenue"
```

**Run a SQL query against loaded data:**
```
"Load user_signups.csv and run: SELECT month, count(*) as signups FROM data GROUP BY month ORDER BY month"
```

**Generate a chart:**
```
"Create a line chart showing monthly revenue over the last 12 months from the sales dataset"
```

**Full analysis workflow:**
```
"Analyze this customer_churn.csv dataset:
1. Identify the top 3 factors correlated with churn
2. Give me 3 actionable recommendations to reduce churn
3. Create a summary report with key metrics"
```

## Requirements

- **Binaries:** `python3`, `pandas`, `matplotlib`, `sqlalchemy` (or equivalent)
- **API Keys:** None
- **Platform:** All

## Tips & Gotchas

- For large datasets (>100k rows), consider loading to SQLite first for faster queries
- Always validate data cleaning steps before running analysis — garbage in, garbage out
- Chart generation may require additional dependencies (e.g., `seaborn` for nicer charts)
- Export raw data alongside reports so you can verify results
- For more complex analysis, use [Data Analysis Skill](https://clawhub.ai/ivangdavila/data-analysis) as a complement

## Related Skills

- [Excel / XLSX](./excel-xlsx.md) — Work directly with Excel files
- [CSV Parser](https://clawhub.ai/gtrusler/csv-parser) — Fast CSV parsing for large files
- [Filesystem Management](./filesystem-management.md) — Load and save datasets from disk
- [Summarize](./summarize.md) — Summarize long analysis reports
