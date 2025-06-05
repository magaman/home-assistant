## 🐞 Bug Zapper - Noon to Dawn with Rain Check (v1.0)

This Home Assistant automation blueprint turns on an outdoor bug zapper at **noon** if the weather is dry, and turns it off at **dawn** or if it starts raining. If it was raining at noon, it remembers this and will **turn the zapper on later** when the rain stops (as long as it's still before dawn).

### 💡 Features
- Turns on a switch at **12:00 PM** if weather is not `rainy`
- Turns **off at dawn** (sunrise) or immediately if it starts raining
- If it was rainy at noon, it will turn the zapper **on when the rain clears**, only before dawn
- Uses an `input_boolean` helper to track rain-delayed activations

---

### 🧰 Requirements
- A Home Assistant instance
- A weather condition sensor (e.g., `sensor.openweathermap_condition`)
- A switch entity controlling the zapper (e.g., `switch.outdoor_plug_2`)
- An `input_boolean` helper to track rain hold

---

### 🛠️ Helper Setup

Create this helper in `configuration.yaml` or via **Settings > Devices & Services > Helpers**:

```yaml
input_boolean:
  bug_zapper_rain_hold:
    name: Bug Zapper Rain Hold
    icon: mdi:weather-rainy
```

---

### 📥 Installation

1. Save the blueprint YAML file as:

```
config/blueprints/automation/[your_username]/bug_zapper_rain.yaml
```

2. In Home Assistant, go to **Settings > Automations & Scenes > Blueprints > Import Blueprint**
3. Choose **"Bug Zapper - Noon to Dawn with Rain Check (v1.0)"**
4. Configure the automation:
   - **Bug Zapper Switch**: Your zapper plug/switch entity
   - **Weather Condition Sensor**: Your weather sensor (e.g., OpenWeather)
   - **Rain Hold Input Boolean**: The `input_boolean.bug_zapper_rain_hold` you created

---

### 🧪 Example Entities
```yaml
switch:
  - platform: tplink
    host: 192.168.1.100
    name: outdoor_plug_2

sensor:
  - platform: openweathermap
    api_key: YOUR_API_KEY
    monitored_conditions:
      - weather
```
