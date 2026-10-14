# CampAware - AI Development Rules

## Before Making Changes

Read the root README, this file, `docs/architecture.md` and `docs/API_CONTRACT.md` before modifying project code.

## Technology Decisions

- ESP32 with Arduino C++
- PMS5003 particulate sensor over UART
- BME280 temperature and humidity sensor over I2C
- HTML, CSS, vanilla JavaScript and Chart.js
- Local HTTP communication between ESP32 and dashboard
- Browser-side storage for initial event logs

Do not introduce a new framework, database, cloud service or library without approval from the integration lead.

## Mandatory Rules

1. Work only on the assigned task and files.
2. Preserve existing working functionality.
3. Do not rename agreed files, API fields or folders without approval.
4. Keep the code understandable to beginner CSE students.
5. Explain significant code changes and dependencies.
6. Clearly distinguish real sensor readings from simulated data.
7. Handle missing, stale and disconnected sensor data.
8. Do not invent hardware pinouts; verify module specifications.
9. Never hardcode secrets or Wi-Fi passwords into committed files.
10. Never claim a test passed unless it was actually run.
11. Do not commit, push or merge unless explicitly authorized.
12. If a change affects another module, coordinate with its owner.
13. If requirements conflict, ask for clarification rather than redesigning the system.
14. Report modified files, tests performed, results and remaining issues.

## Git Rules

- Work on a task-specific branch.
- Pull the latest main branch before starting.
- Avoid simultaneous edits to the same files.
- Review changes before committing.
- Merge through a pull request after review.
- Never force-push to main.

## Definition of Done

A task is complete when the assigned feature is implemented, the relevant tests have been run where possible, limitations are documented and the changes are ready for review.