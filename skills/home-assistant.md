# Home Assistant

> Control your smart home directly from your agent — turn on lights, adjust thermostats, run automations, get sensor readings.

**ClawHub:** https://clawhub.ai/iAhmadZain/home-assistant · ⭐ 36 · 142 installs  
**License:** MIT-0 · **API Key:** 🔑 Required — Home Assistant Long-Lived Access Token  
**Security:** ✅ Clean (VirusTotal: Benign · OpenClaw: Benign)

---

## What It Does

Home Assistant skill gives your agent full control over your Home Assistant instance. Toggle lights, adjust thermostats, run automations, get sensor readings, receive notifications when events happen — all from your chat. Perfect for building voice-controlled or automated smart home workflows.

## How to Install

```bash
clawhub install home-assistant
```

**Setup:**
1. In Home Assistant: Create a Long-Lived Access Token (Settings > People > Select User > Create Token)
2. Set env vars:
   ```bash
   export HOME_ASSISTANT_URL="https://your-home-assistant-url.com"
   export HOME_ASSISTANT_TOKEN="your-long-lived-token"
   ```

## Key Capabilities

- Control smart devices: lights, switches, thermostats, plugs, cameras
- Get real-time sensor readings: temperature, humidity, power usage, presence
- Run automations and scripts
- Receive notifications when events happen
- Query state of any entity in your Home Assistant instance
- Toggle scenes and groups

## Usage Examples

**Control a light:**
```
"Turn on the living room light and set brightness to 70%"
```

**Get sensor readings:**
```
"What's the current temperature in the bedroom?"
"How much power is the house using right now?"
```

**Run an automation:**
```
"Run the 'Good Night' automation"
```

**Check entity state:**
```
"Is the front door locked?"
"Is the garage door open?"
```

**Adjust thermostat:**
```
"Set the thermostat to 21°C"
```

## Requirements

- **Binaries:** None (HTTP API calls)
- **API Keys:** Home Assistant Long-Lived Access Token
- **Platform:** All
- **Prerequisite:** Running Home Assistant instance accessible over the network

## Tips & Gotchas

- Use least privilege: create a separate user for the agent with only the permissions it needs
- If your Home Assistant instance is not publicly accessible, run the agent on the same local network
- Entity IDs are case-sensitive: `light.living_room` not `Light.Living_Room`
- Pair with [Proactive Agent](./proactive-agent.md) for automated alerts (e.g., "front door opened while you're away")

## Related Skills

- [Weather](./weather.md) — Use weather data to trigger smart home automations
- [Calendar Integration](https://clawhub.ai/Asleep123/caldav-calendar) — Sync calendar events with home automations
- [Proactive Agent](./proactive-agent.md) — Smart home notifications and alerts
