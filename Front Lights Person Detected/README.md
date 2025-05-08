# 👤✨ Person Detected Light Control (Grouped)

## 📋 Overview
This Home Assistant automation blueprint turns on groups of lights (porch, front yard, driveway) when a person is detected, but only if it is after sunset and before sunrise. Each group has its own configurable auto-off timer.

## 📁 Installation
1. Copy the `person_detected_lights_grouped.yaml` file into your Home Assistant config folder under:
   ```
   config/blueprints/automation/[your_name]/person_detected_lights_grouped.yaml
   ```
2. Restart Home Assistant or go to *Settings → Automations & Scenes → Blueprints* and reload blueprints.
3. Create a new automation using the "👤✨ Person Detected Light Control (Grouped)" blueprint.

## ⚙️ Options
- **Person Detection Sensors**: One or more binary sensors that detect motion/person (e.g. cameras or motion sensors).
- **Light Groups**: Separate inputs for Porch, Front Yard, and Driveway.
- **Delays**: Each group has its own delay for how long to keep the lights on before turning them off.

## 🧠 Tips
- Set a `mode: single` and `max_exceeded: silent` is included to avoid automation overlap.
- The automation only runs during nighttime hours (sunset to sunrise).
