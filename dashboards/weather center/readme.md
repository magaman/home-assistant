# 🏠 My Home Assistant Configuration

Welcome to my Home Assistant repository! This is a collection of my personal configurations, custom dashboards, and automation blueprints.

## 🌤️ Featured Dashboard: Weather & Energy Center
This dashboard provides a high-density "Weather Station" view, combining local meteorological data with energy status (Tesla Powerwall) and AI-driven space weather alerts.

### 📸 Screenshot Gallery
| | | |
|:---:|:---:|:---:|
| <img src="screenshots/weather1.png" width="300"> | <img src="screenshots/weather2.png" width="300"> | <img src="screenshots/weather3.png" width="300"> |
| **Full Dashboard Overview** <br> *Complete grid-based layout.* | **Severe Weather & Energy** <br> *NWS alerts and Powerwall status.* | **Space Weather Alert** <br> *Detailed flare and blackout risks.* |
| <img src="screenshots/weather4.png" width="300"> | <img src="screenshots/weather5.png" width="300"> | <img src="screenshots/weather6.png" width="300"> |
| **Quiet Space Weather** <br> *Status during low solar activity.* | **Live Tracking** <br> *Windy radar and lightning detection.* | **Dynamic Weather States** <br> *UI changes (e.g., Snow ring) based on conditions.* |

---

## 🧩 Dependencies

### 1. Custom Cards (HACS)
| Card | Description | Source |
| :--- | :--- | :--- |
| **Ring Tile Card** | Circular gauges for wind, UV, and sensors | [GitHub](https://github.com/neponn/ring-tile-card) |
| **Hourly Weather** | Horizontal bar-style hourly forecast | [GitHub](https://github.com/decompil3d/lovelace-hourly-weather) |
| **Clock Weather** | Integrated date and weather summary row | [GitHub](https://github.com/pkissling/clock-weather-card) |
| **Lunar Phase** | Visual moon phase tracking | [GitHub](https://github.com/ngocjohn/lunar-phase-card) |
| **Blitzortung Lightning** | Real-time strike map and history | [GitHub](https://github.com/timmaurice/lovelace-blitzortung-lightning-card) |

### 2. Required Integrations
The data and logic are powered by these essential integrations:
* **[Enhanced Input](https://github.com/yohaybn/HomeAssistant-Enhanced-Input)**: Used to store long-form AI space weather alerts that exceed standard 255-character limits.
* **Weather:** [OpenWeatherMap](https://www.home-assistant.io/integrations/openweathermap/), [NWS Alerts](https://github.com/Snuffy2/nws_alerts_array), [NOAA Space Weather](https://github.com/tcarwash/home-assistant_noaa-space-weather).
* **Energy:** [Tesla Fleet](https://github.com/alandtse/tesla) (Powerwall Status/Storm Watch).
* **Environmental:** [Blitzortung Lightning](https://github.com/mrk-its/homeassistant-blitzortung), [World Air Quality Index (WAQI)](https://www.home-assistant.io/integrations/waqi/).

---

## ⚙️ Key Features

### 🌌 AI-Driven Space Weather
Uses a custom automation and **Google AI (Gemini)** to generate concise, human-readable alerts for Holbrook, NY. 
* Triggered by high Kp index (>5.5) or high M-Class flare probability (>50%).
* Responses are stored via the **Enhanced Input** integration to ensure full readability of the AI summary.
* Automatically clears to a "No active alerts" success state when conditions normalize.

### ⚡ Powerwall Intelligence
The dashboard monitors for **Tesla Storm Watch** activation. It dynamically calculates battery levels and power flow (kW), changing the UI to a warning state during grid instability events to ensure system readiness.

### 🌧️ Reactive Environmental Rings
Using **Conditional Cards**, the UI swaps specific rings based on current conditions:
* Displays **Rain** or **Snow** accumulation during active precipitation.
* Reverts to **UV Index** or **Cloud Coverage** during clear weather.

---

## 🏗️ Blueprints & Automations
* [`/automations/space_weather.yaml`](./automations/space_weather.yaml): The AI logic for generating space weather reports.

## 🛠️ Installation
1. Install **Enhanced Input** and all **Custom Cards** via HACS.
2. Configure your integrations (OpenWeatherMap, Tesla Fleet, etc.).
3. Add the Space Weather automation to your instance.
4. Copy the view YAML from [`dashboards/weather.yaml`](./dashboards/weather.yaml) into your dashboard's Raw Configuration Editor.

---
**Happy Automating!**
