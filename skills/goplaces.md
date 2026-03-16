# GoPlaces

> Location-aware place search, navigation, and local business lookup. Find nearby restaurants, stores, ATMs, and more.

**ClawHub:** https://clawhub.ai/steipete/goplaces · ⭐ 26 · 901 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — Google Places or OpenStreetMap API key  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

GoPlaces lets your agent search for local businesses, places of interest, get directions, and find nearby services: restaurants, cafes, ATMs, gas stations, hotels, and more. Perfect for travel and local discovery.

## How to Install

```bash
clawhub install goplaces
```

**Setup:**
1. Get a Google Places API key or OpenStreetMap Nominatim API key
2. Set env var: `export PLACES_API_KEY="your-key"`

## Key Capabilities

- Search for nearby places by category: restaurants, cafes, hotels, ATMs, etc.
- Get place details: address, phone number, opening hours, ratings, reviews
- Get directions between locations
- Search places by name
- Filter by rating, distance, and opening status

## Usage Examples

**Find nearby restaurants:**
```
"Find the top 5 rated Italian restaurants within 1 mile of my current location that are open now"
```

**Get place details:**
```
"Get the address and opening hours for Central Perk Cafe in New York"
```

**Get directions:**
```
"Give me walking directions from my current location to the nearest subway station"
```

## Requirements

- **Binaries:** None
- **API Keys:** Google Places API key or OpenStreetMap Nominatim key
- **Platform:** All
- **Optional:** Location access for current location queries

## Tips & Gotchas

- Google Places API has usage costs — monitor your usage to avoid unexpected charges
- OpenStreetMap Nominatim is free but has rate limits
- Location access required for "near me" queries
- Pair with [Weather](./weather.md) for travel planning

## Related Skills

- [Weather](./weather.md) — Check weather for travel destinations
- [Calendar Integration](./caldav-calendar.md) — Sync travel plans with your calendar
