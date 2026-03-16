# Gog

> Game launcher and library management skill for GOG.com. Launch games, view library, manage installations.

**ClawHub:** https://clawhub.ai/steipete/gog · ⭐ 741 · installs: N/A  
**License:** MIT-0 · **API Key:** 🔑 Required — GOG account credentials  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Gog skill lets your agent interact with your GOG.com game library: view installed games, launch games, manage installations, and browse your game collection. For gamers who use GOG as their primary game platform.

## How to Install

```bash
clawhub install gog
```

**Setup:**
1. Install [GOG Galaxy](https://www.gog.com/galaxy)
2. Authenticate with your GOG account credentials
3. Set env vars for GOG API access if needed

## Key Capabilities

- List all games in your GOG library
- Launch installed games
- Install/uninstall games
- View game details: playtime, last played, install size
- Search your game library
- Check for game updates

## Usage Examples

**Launch a game:**
```
"Launch Cyberpunk 2077 from my GOG library"
```

**List installed games:**
```
"Show me all installed games in my GOG library"
```

**Check playtime:**
```
"How many hours have I played The Witcher 3?"
```

## Requirements

- **Binaries:** GOG Galaxy client
- **API Keys:** GOG account credentials
- **Platform:** Windows · macOS · Linux

## Tips & Gotchas

- Requires GOG Galaxy to be running in the background
- Only works with games you own on GOG.com
- Limited automation capabilities due to GOG API restrictions

## Related Skills

- [Steam Integration](https://clawhub.ai/steipete/steam) — Alternative for Steam users
