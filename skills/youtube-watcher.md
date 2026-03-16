# YouTube Watcher

> Extract transcripts from any YouTube video — then summarize, search, or Q&A the content without watching a single second.

**ClawHub:** https://clawhub.ai/Michaelgathara/youtube-watcher · ⭐ 217 · 331 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

YouTube Watcher uses `yt-dlp` to pull closed captions or auto-generated subtitles from any YouTube video and returns the full transcript as text. Your agent then reads, summarizes, searches, or answers questions about the content — no video to watch, no scraping fragile web APIs.

⭐217 · 331 installs. Core research and content analysis skill.

> **Note from community:** Some users report YouTube blocking certain requests. If transcripts fail, try a different video or use the Summarize skill's `--youtube auto` flag with an Apify token as fallback.

## How to Install

```bash
clawhub install youtube-watcher
```

**Prerequisite:** Install `yt-dlp`:
```bash
brew install yt-dlp          # macOS
pip install yt-dlp           # pip (all platforms)
```

## Key Capabilities

- Fetch full transcript from any YouTube video
- Works with CC (closed captions) and auto-generated subtitles
- Returns plain text — ready for summarization or search
- Search for specific keywords within a transcript
- Answer questions about video content
- Bulk transcript extraction across multiple videos

## Usage Examples

**Get a video transcript:**
```bash
python3 {baseDir}/scripts/get_transcript.py "https://www.youtube.com/watch?v=VIDEO_ID"
```

**Summarize a video (two-step):**
```
1. Get transcript:
   python3 {baseDir}/scripts/get_transcript.py "https://youtu.be/VIDEO_ID"

2. Agent reads and summarizes the output
```

**Ask questions about a video:**
```
"Fetch the transcript for https://youtu.be/VIDEO_ID,
then tell me: what are the three main arguments the speaker makes?"
```

**Find timestamps for a topic:**
```
"Get the transcript for [URL], then find all sections
where they discuss [topic] and give me the timestamps."
```

## Requirements

- **Binaries:** `yt-dlp`, `python3`
- **API Keys:** None
- **Platform:** macOS · Linux · Windows

## Tips & Gotchas

- Only works on videos that have subtitles (CC or auto-generated) — videos without subtitles will fail
- YouTube rate-limits aggressive requests — don't loop over many videos too fast
- `yt-dlp` needs to be kept updated: `pip install --upgrade yt-dlp` (YouTube changes their API frequently)
- For videos where yt-dlp is blocked, use [Summarize](./summarize.md) with `--youtube auto` + `APIFY_API_TOKEN`
- Transcript quality varies — auto-generated subs can have errors, especially for technical terms

## Related Skills

- [Summarize](./summarize.md) — Summarize video content with optional Apify fallback
- [Deep Research Pro](./deep-research-pro.md) — Include video content in multi-source research
- [Brave Search](./brave-search.md) — Find relevant videos to analyze
