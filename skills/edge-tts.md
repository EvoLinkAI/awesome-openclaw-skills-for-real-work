# Edge TTS

> Free, high-quality text-to-speech using Microsoft Edge voices. No API keys, no rate limits.

**ClawHub:** https://clawhub.ai/i3130002/edge-tts · ⭐ 22 · 151 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Edge TTS gives your agent access to Microsoft's high-quality text-to-speech voices for free, no API keys, no rate limits. Generate natural-sounding audio from any text in multiple languages and voices. Perfect for creating audio versions of documents, voiceovers, or accessibility features.

## How to Install

```bash
clawhub install edge-tts
```

**Prerequisite:** Install the `edge-tts` Python package:
```bash
pip install edge-tts
```

## Key Capabilities

- Free, no API keys, no rate limits
- 100+ voices across 40+ languages
- Adjustable speech rate, volume, and pitch
- Supports SSML (Speech Synthesis Markup Language)
- Output MP3 or WAV audio files
- List all available voices

## Usage Examples

**Basic text-to-speech:**
```bash
edge-tts --text "Hello world, this is a test" --write-media output.mp3
```

**List all available voices:**
```bash
edge-tts --list-voices
```

**Use a specific voice and adjust rate:**
```bash
edge-tts --voice en-US-AndrewNeural --rate +10% --text "Hello from Edge TTS" --write-media output.mp3
```

**Adjust pitch and volume:**
```bash
edge-tts --pitch +5% --volume +10% --text "Welcome to the demo" --write-media output.mp3
```

**Generate long-form audio from a file:**
```bash
edge-tts --file input.txt --write-media audiobook.mp3
```

## Requirements

- **Binaries:** `python3`, `edge-tts`
- **API Keys:** None
- **Platform:** macOS · Linux · Windows

## Tips & Gotchas

- Voices are maintained by Microsoft — quality is consistently high
- Speech rate range: -50% (half speed) to +100% (double speed)
- For long texts, split into chunks to avoid timeouts
- SSML support lets you add pauses, emphasis, and other speech effects
- Perfect for generating audio versions of long documents or blog posts

## Related Skills

- [OpenAI Whisper](./openai-whisper.md) — Speech-to-text complement to TTS
- [YouTube Watcher](./youtube-watcher.md) — Generate transcripts, then turn them into audio
- [Summarize](./summarize.md) — Summarize text before converting to audio
