# Weather

> Current weather and 3-day forecast for any location — no API key, no setup, works everywhere.

**ClawHub:** https://clawhub.ai/steipete/weather · ⭐ 294 · 2,400 installs  
**License:** MIT-0 · **API Key:** 🆓 Not required  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign, high confidence)

---

## What It Does

Weather uses `wttr.in` (primary) and Open-Meteo (fallback) to get current conditions and forecasts for any location in the world — city names, airport codes, coordinates. No API keys, no accounts, just `curl`. One of the simplest and most reliable skills in the ecosystem.

⭐294 · 2,400 installs — consistently one of the most popular skills.

## How to Install

```bash
clawhub install weather
```

## Key Capabilities

- Current conditions: temperature, humidity, wind speed and direction
- 3-day forecast
- Airport code support (e.g., `JFK`, `LHR`)
- Metric or USCS units
- Moon phase
- PNG weather map
- Open-Meteo JSON fallback for programmatic use

## Usage Examples

**Quick current weather:**
```bash
curl -s "wttr.in/London?format=3"
# London: ⛅️ +8°C

curl -s "wttr.in/Tokyo?format=3"
# Tokyo: 🌤️ +22°C
```

**Compact format with humidity and wind:**
```bash
curl -s "wttr.in/Paris?format=%l:+%c+%t+%h+%w"
# Paris: ⛅️ +15°C 65% ↙12km/h
```

**Full 3-day forecast:**
```bash
curl -s "wttr.in/Berlin?T"
```

**Airport code:**
```bash
curl -s "wttr.in/SFO?format=3"
```

**Save weather map as PNG:**
```bash
curl -s "wttr.in/Berlin.png" -o /tmp/weather.png
```

**Open-Meteo JSON (programmatic):**
```bash
# London coordinates: lat=51.5, lon=-0.12
curl -s "https://api.open-meteo.com/v1/forecast?latitude=51.5&longitude=-0.12&current_weather=true"
# Returns: temp, windspeed, weathercode, is_day
```

## Format Codes (wttr.in)

| Code | Meaning |
|------|---------|
| `%c` | Condition emoji |
| `%t` | Temperature |
| `%h` | Humidity |
| `%w` | Wind |
| `%l` | Location |
| `%m` | Moon phase |

## URL Options

| Option | Effect |
|--------|--------|
| `?format=3` | One-line compact |
| `?1` | Today's forecast only |
| `?0` | Current conditions only |
| `?m` | Metric units |
| `?u` | USCS units |
| `?T` | Full text forecast |

## Requirements

- **Binaries:** `curl`
- **API Keys:** None
- **Platform:** All

## Tips & Gotchas

- URL-encode spaces: `wttr.in/New+York` not `wttr.in/New York`
- Queries include your location — if privacy matters, be aware wttr.in logs queries
- Open-Meteo requires coordinates, not city names — use a geocoding API first if needed
- Use `?0` for "right now" only — `?1` gives today's full day forecast

## Related Skills

- [GoPlaces](https://clawhub.ai/steipete/goplaces) — Location-aware place search
- [Home Assistant](https://clawhub.ai/iAhmadZain/home-assistant) — Use weather data to trigger automations
