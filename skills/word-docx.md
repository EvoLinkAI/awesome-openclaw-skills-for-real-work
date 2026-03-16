# Word / DOCX

> Create, read, edit, and format Microsoft Word documents directly from your agent.

**ClawHub:** https://clawhub.ai/ivangdavila/word-docx · ⭐ 62 · 191 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Word DOCX skill lets your agent work with .docx files — create new documents, read content from existing ones, edit text, apply formatting, add images/headers/footers, and export to PDF/Markdown. Automate report generation, document editing, and content workflows without Microsoft Word.

## How to Install

```bash
clawhub install word-docx
```

## Key Capabilities

- Read text content from Word documents
- Create new Word documents with formatted text
- Apply formatting: bold, italic, underline, headings, lists
- Add tables, images, headers, footers, page breaks
- Replace placeholder text in templates
- Export Word documents to Markdown or PDF
- Bulk process multiple Word files

## Usage Examples

**Read a Word document:**
```
"Extract all text from report.docx and summarize it for me"
```

**Create a new report from template:**
```
"Create a Word document using the template:
Title: Q1 2026 Performance Report
Section 1: Executive Summary [content here]
Section 2: Key Metrics [table here]
Save as q1_performance.docx"
```

**Replace placeholders in a template:**
```
"Load the contract_template.docx file and replace {{CLIENT_NAME}} with 'Acme Corp',
{{DATE}} with '2026-03-16', {{AMOUNT}} with '$12,500'"
```

**Export to PDF:**
```
"Convert the q1_performance.docx file to PDF"
```

## Requirements

- **Binaries:** `python3`, `python-docx` (for editing), `pandoc` (for PDF export)
- **API Keys:** None
- **Platform:** All

## Tips & Gotchas

- Only works with .docx files — older .doc files need conversion
- Complex formatting and macros are not supported
- PDF export requires Pandoc and a LaTeX distribution (or LibreOffice)
- Always back up original files before making edits
- For best results, use simple templates with clear placeholders

## Related Skills

- [Excel / XLSX](./excel-xlsx.md) — Work with Excel files
- [Summarize](./summarize.md) — Summarize content extracted from Word documents
- [Notion](./notion.md) — Import/export content between Word and Notion
