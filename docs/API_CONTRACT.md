# CampAware API Contract

## Purpose

Define the JSON format shared between ESP32 firmware and the web dashboard.

## Planned Endpoint

`GET /api/readings`

The firmware implementation must return a JSON response following the agreed format.

## Example Response

```json
{
  "pm1_0": 12,
  "pm2_5": 18,
  "pm10": 24,
  "temperature_c": 29.4,
  "humidity_percent": 58,
  "timestamp": "2026-10-14T10:30:00Z",
  "status": "ok",
  "data_source": "real"
}
```

The values above are illustrative only, not actual measurements.

## Field Definitions

| Field | Meaning | Unit |
|---|---|---|
| `pm1_0` | PM1.0 concentration | µg/m³ |
| `pm2_5` | PM2.5 concentration | µg/m³ |
| `pm10` | PM10 concentration | µg/m³ |
| `temperature_c` | Temperature | °C |
| `humidity_percent` | Relative humidity | % |
| `timestamp` | Measurement timestamp in ISO 8601 format | UTC |
| `status` | Overall reading status | Text |
| `data_source` | Origin of the displayed data | `real` or `simulated` |

## Rules

- Both firmware and dashboard must use the same field names.
- Particulate readings must use the same agreed concentration units.
- Missing or invalid values must not be presented as genuine zero readings.
- The dashboard must show stale or disconnected data visibly.
- Simulated data must always be labelled as simulated.
- The dashboard must not treat PM2.5 alone as official AQI.
- Timestamp handling and error-response behavior must be agreed before integration.

## Status Values

The initial planned status values are `ok`, `stale`, `disconnected` and `error`.

These values describe data availability and device operation, not whether air is safe.

## Change Management

Changes to this contract require agreement from both the firmware owner and dashboard owner, with the documentation updated in the same change.