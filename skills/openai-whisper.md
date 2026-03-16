# OpenAI Whisper

> Speech-to-text transcription using OpenAI Whisper API. Convert audio files to text with high accuracy.

**ClawHub:** https://clawhub.ai/steipete/openai-whisper · ⭐ 213 · installs: N/A  
**License:** MIT-0 · **API Key:** 🔑 Required — `OPENAI_API_KEY`  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

OpenAI Whisper skill lets your agent transcribe audio files to text using OpenAI's Whisper API. It supports multiple languages, handles accents and background noise well, and produces highly accurate transcriptions. Perfect for converting podcasts, meetings, voice notes, and videos to text.

## How to Install

```bash
clawhub install openai-whisper
```

**Setup:**
1. Get your OpenAI API key from [platform.openai.com/api-keys](https://platform.openai.com/api-keys)
2. Set env var: `export OPENAI_API_KEY="your-key"`

## Key Capabilities

- Transcribe audio files to text (MP3, WAV, M4A, and more)
- Support for 99+ languages
- Automatic language detection
- Timestamped transcriptions (word-level or segment-level)
- Translate non-English audio to English
- High accuracy even with background noise or accents

## Usage Examples

**Transcribe an audio file:**
```
"Transcribe this meeting.mp3 file and return the full text"
```

**Translate non-English audio to English:**
```
"Transcribe this Japanese audio file and translate it to English"
```

**Get timestamped transcription:**
```
"Transcribe this podcast.mp3 file with timestamps for each segment"
```

## Requirements

- **Binaries:** None (API-based)
- **API Keys:** `OPENAI_API_KEY`
- **Platform:** All
- **Note:** Local Whisper models are also available for offline use (additional setup required)

## Tips & Gotchas

- Maximum audio file size: 25MB
- For longer audio files, split into chunks first
- Whisper API is very affordable: ~$0.006 per minute of audio
- Pair with [Summarize](./summarize.md) to summarize transcripts after transcription
- For free local transcription, use the open-source Whisper model locally instead of the API

## Related Skills

- [Edge TTS](./edge-tts.md) — Text-to-speech complement to Whisper
- [Summarize](./summarize.md) — Summarize transcribed audio
- [YouTube Watcher](./youtube-watcher.md) — Transcribe YouTube videos
