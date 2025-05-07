# home-assistant

# Bug Zapper Automation
📝 Instructions to Use
Create the input boolean via UI or YAML:

yaml
Copy
Edit
input_boolean:
  bug_zapper_rain_hold:
    name: Bug Zapper Rain Hold
Import this blueprint into Home Assistant (Settings > Automations & Scenes > Blueprints > Import Blueprint) by pasting this YAML in a file under:

swift
Copy
Edit
config/blueprints/automation/your_username/bug_zapper_rain.yaml
Create a new automation using this blueprint and select:

The zapper switch

Your weather condition sensor (like sensor.openweathermap_condition)

The input boolean (input_boolean.bug_zapper_rain_hold)
