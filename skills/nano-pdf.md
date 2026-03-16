# Nano PDF

> Ultra-lightweight PDF reader — extract text from any PDF file without heavy dependencies.

**ClawHub:** https://clawhub.ai/steipete/nano-pdf · ⭐ 147 · installs: N/A  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Nano PDF is a minimal, dependency-free PDF text extractor. It pulls readable text from any PDF file quickly, no heavy Java-based tools or large dependencies required. Perfect for quick text extraction from PDFs without the overhead of full PDF processing libraries.

## How to Install

```bash
clawhub install nano-pdf
```

## Key Capabilities

- Extract plain text from any PDF file
- Lightweight, no heavy dependencies
- Fast extraction for small to medium PDFs
- Works with password-protected PDFs (if you provide the password)
- Command-line interface for easy integration with other tools

## Usage Examples

**Extract text from a PDF:**
```bash
nano-pdf input.pdf output.txt
```

**Extract text to stdout:**
```bash
nano-pdf input.pdf
```

**Extract from a password-protected PDF:**
```bash
nano-pdf --password "your-password" protected.pdf output.txt
```

**Extract specific pages:**
```bash
nano-pdf --pages 1-5,10 input.pdf output.txt
```

## Requirements

- **Binaries:** `nano-pdf` (included with the skill)
- **API Keys:** None
- **Platform:** macOS · Linux · Windows

## Tips & Gotchas

- For scanned PDFs (image-only), you need OCR software first — nano-pdf only works with text-based PDFs
- Extraction quality varies depending on how the PDF was created
- For complex PDFs with tables and complex formatting, use a more feature-rich PDF processing tool
- Pair with [Summarize](./summarize.md) to summarize the extracted text immediately

## Related Skills

- [Summarize](./summarize.md) — Summarize extracted PDF text
- [Data Analyst](./data-analyst.md) — Analyze data extracted from PDF reports
- [Filesystem Management](./filesystem-management.md) — Batch process multiple PDF files
