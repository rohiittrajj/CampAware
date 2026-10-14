# CampAware

**Smarter Monitoring. Healthier Campuses.**

CampAware is an IoT-based campus environmental monitoring prototype designed to measure particulate matter and basic environmental conditions.

## Objectives

- Measure PM1.0, PM2.5 and PM10 using the PMS5003 sensor.
- Measure temperature and humidity using the BME280 sensor.
- Display readings on a web dashboard.
- Record contextual events, such as cleaning or opening windows.
- Compare measurements before and after recorded events.
- Show whether data is real, simulated, stale or unavailable.

## Technology Stack

- **Hardware:** ESP32, PMS5003, BME280
- **Firmware:** Arduino C++
- **Dashboard:** HTML, CSS, JavaScript and Chart.js
- **Communication:** Local HTTP API with JSON
- **Collaboration:** Git and GitHub

## Project Structure

- `firmware/` — ESP32 firmware
- `dashboard/` — Web dashboard
- `docs/` — Architecture, API contract, wiring and testing instructions
- `tests/` — Test data and test resources

## Development Rules

1. Read `docs/AI_RULES.md` before using an AI tool to modify the project.
2. Follow `docs/API_CONTRACT.md` when working on firmware or dashboard integration.
3. Use task-specific Git branches and pull requests.
4. Never commit passwords, Wi-Fi credentials or API secrets.
5. Clearly label simulated data.
6. Test changes before requesting a merge.

## Project Status

Development environment setup and hardware integration are in progress.

## Important Limitation

CampAware is a student prototype, not a certified air-quality instrument. Its particulate measurements do not establish overall indoor air safety or official AQI.