# NexGenEV Dashboard — Separate Files

Keep these three files together:

- index.html — page structure
- style.css — design and layout
- script.js — simulation, fuzzy inference, chart, CSV and USB Serial

Open this folder in VS Code. Right-click index.html and choose Open with Live Server (install the Live Server extension first). Use desktop Chrome or Edge for USB Serial. No npm install is required.

Simulation runs immediately. For actual sensor input, close Arduino Serial Monitor, select the correct baud rate and click Connect ESP32. Send numeric temperature (Celsius) and current (amperes) as newline-delimited JSON:

```json
{"temperature":32.4,"current":2.5}
```

Fuzzy inference runs in the browser, not ESP32. No pump commands are transmitted. Pump status remains unverified. Sensor-specific ESP32 firmware is not included because sensor models/pins are unknown. Default thresholds are illustrative and are not validated battery safety limits.

The embedded file viewer may not load sibling CSS/JS files. Download/extract the complete ZIP and run locally for the full dashboard.
