# 👤✨ Person Detected Light Control (Grouped, Optional)

## 📋 Overview
This Home Assistant automation blueprint turns on selected groups of lights (porch, front yard, driveway) when a person is detected,
but only if it’s within a user-defined time window (default: sunset to sunrise). Each group has its own auto-off delay.

## 🛠️ Features
- 🧠 Person detection via one or more binary sensors
- 🔦 Control any combination of light groups
- ⏱️ Individual auto-off delays per group
- 🌙 Time window control (default sunset to sunrise)
- 🛑 Cooldown prevention with `mode: single`

## 📁 Installation
1. Save `person_detected_lights_grouped.yaml` into:
   ```
   config/blueprints/automation/[your_name]/person_detected_lights_grouped.yaml
   ```
2. Restart Home Assistant or reload blueprints from the UI.
3. Go to *Settings → Automations & Scenes → Blueprints → Create Automation* and select this blueprint.

## ⚙️ Options
- **Person Detection Sensors**: Motion or person binary sensors.
- **Enable Light Groups**: Choose which zones to use.
- **Delays**: Customize shutoff time for each zone.
- **Time Window**: Define when automation is allowed to run.

