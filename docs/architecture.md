# CampAware Architecture

## Overview

CampAware is an IoT-based environmental monitoring prototype with four main parts.

1. **Sensors:** PMS5003 measures particulate matter; BME280 measures temperature and humidity.
2. **ESP32 firmware:** Reads sensor data and manages Wi-Fi and the local HTTP API.
3. **Web dashboard:** Displays measurements, charts, event logs and comparisons.
4. **Browser storage:** Stores initial event logs locally in the user's browser.

## Data Flow

Sensors → ESP32 → Local HTTP API → Web Dashboard

The dashboard must distinguish live readings from simulated readings and clearly indicate stale or unavailable data.

## Technology

- ESP32 with Arduino C++
- PMS5003 over UART
- BME280 over I2C
- HTML, CSS and JavaScript
- Chart.js
- Git and GitHub for collaboration

## Initial Scope

The first working version should:

- Display particulate matter, temperature and humidity.
- Show data source and connection status.
- Record contextual events with timestamps.
- Display measurements over time.
- Compare measurements from two selected periods.
- Export collected readings where practical.

## Limitations

- The PMS5003 does not measure every air pollutant.
- PM2.5 measurements alone are not official AQI.
- Before-and-after differences do not prove that an event caused the change.
- Browser-side event storage is local to that browser unless export or synchronization is implemented.

## Integration Rules

- The firmware and dashboard must follow `docs/API_CONTRACT.md`.
- Hardware pins must be verified against the exact modules and cables.
- Changes affecting both firmware and dashboard require coordination.
- Prefer a working, tested feature over an untested advanced feature.