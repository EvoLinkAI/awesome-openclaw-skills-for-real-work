# Excel / XLSX

> Read, write, edit, and analyze Excel files directly from your agent — no Excel installation required.

**ClawHub:** https://clawhub.ai/ivangdavila/excel-xlsx · ⭐ 40 · 186 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Excel skill lets your agent read and write .xlsx files, manipulate worksheets, extract data, run formulas, and analyze spreadsheet content — no Microsoft Excel or Google Sheets needed. Perfect for processing reports, exporting data, and automating spreadsheet workflows.

## How to Install

```bash
clawhub install excel-xlsx
```

## Key Capabilities

- Read Excel files and extract data from specific worksheets
- Create new Excel files with multiple worksheets
- Write data to specific cells/ranges
- Run Excel formulas programmatically
- Format cells (font, color, alignment, borders)
- Pivot table generation
- Export Excel worksheets to CSV/Markdown
- Bulk process multiple Excel files

## Usage Examples

**Extract data from a worksheet:**
```
"Read the 'Sales 2026' worksheet from sales_report.xlsx and give me the total revenue per region"
```

**Create a new Excel file:**
```
"Create an Excel file with two worksheets: 'Revenue' and 'Expenses'
Populate Revenue with the data I gave you earlier"
```

**Add a formula to a cell:**
```
"In the expenses.xlsx file, add a SUM formula to cell B10 that sums B2:B9"
```

**Convert Excel to CSV:**
```
"Convert the 'Q1 Report' worksheet from report.xlsx to CSV"
```

## Requirements

- **Binaries:** `python3`, `openpyxl` (or `pandas` + `openpyxl`)
- **API Keys:** None
- **Platform:** All

## Tips & Gotchas

- Only works with .xlsx files — older .xls files need conversion first
- Complex Excel macros are not supported
- Formulas are evaluated in Python, not in Excel — ensure formula compatibility
- Always back up original files before making edits
- For very large Excel files, convert to CSV first for faster processing

## Related Skills

- [Data Analyst](./data-analyst.md) — Analyze data extracted from Excel files
- [Word / DOCX](./word-docx.md) — Work with Word documents
- [Filesystem Management](./filesystem-management.md) — Load and save Excel files from disk
