# Markdown Converter

> Convert any format to/from Markdown — HTML, DOCX, PDF, plain text, and more. Perfect for content workflows.

**ClawHub:** https://clawhub.ai/steipete/markdown-converter · ⭐ 115 · 239 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Markdown Converter lets you convert almost any document format to/from Markdown. Convert HTML pages, Word DOCX files, PDFs, plain text, and even Google Docs to clean Markdown, or export Markdown to other formats. Essential for content creation, documentation, and note-taking workflows.

## How to Install

```bash
clawhub install markdown-converter
```

**Prerequisite:** Install Pandoc:
```bash
brew install pandoc          # macOS
apt install pandoc           # Debian/Ubuntu
```

## Key Capabilities

- Convert to Markdown: HTML, DOCX, PDF, plain text, reStructuredText, ODT, and more
- Convert from Markdown: HTML, DOCX, PDF, EPUB, plain text, and more
- Clean up messy Markdown (fix headers, lists, links)
- Batch convert multiple files at once
- Preserve formatting where possible (headings, lists, links, images)

## Usage Examples

**Convert HTML to Markdown:**
```bash
pandoc -s input.html -o output.md
```

**Convert DOCX to Markdown:**
```bash
pandoc -s input.docx --extract-media ./images -o output.md
```

**Convert Markdown to PDF:**
```bash
pandoc input.md -o output.pdf
```

**Convert Markdown to DOCX:**
```bash
pandoc input.md -o output.docx
```

**Clean up messy Markdown:**
```bash
markdown-converter --clean messy.md > clean.md
```

## Requirements

- **Binaries:** `pandoc`
- **API Keys:** None
- **Platform:** All

## Tips & Gotchas

- Use `--extract-media` when converting DOCX/PDF to extract images to a separate folder
- For PDFs, text extraction quality varies — use OCR for scanned PDFs
- For best results, use Pandoc 3.0 or later
- Pair with [Notion](./notion.md) or [Obsidian](./obsidian.md) to import converted content directly into your knowledge base

## Related Skills

- [Word / DOCX](./word-docx.md) — Work directly with Word documents
- [Nano PDF](./nano-pdf.md) — Extract text from PDFs before converting
- [Obsidian](./obsidian.md) — Import converted Markdown into your vault
