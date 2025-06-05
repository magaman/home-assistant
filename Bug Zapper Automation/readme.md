## 🐞 Bug Zapper - Flexible Schedule with Rain Check (v2.0)

This blueprint lets you run your outdoor bug zapper on your own schedule.
For the on and off triggers you can choose either a fixed time or a sun event
(sunrise, sunset, dawn or dusk) and mix them however you like. If it starts
raining the zapper is turned off and it will automatically resume once the
weather clears, as long as your chosen off time hasn't passed.

### 💡 Features
- Select a time or sun event to turn the zapper **on**
- Select a time or sun event to turn the zapper **off**
- Mix time and sun triggers however you like
- Pauses operation while raining and resumes when dry
- Uses an `input_boolean` helper to track rain-delayed starts

---

### 🧰 Requirements
- A Home Assistant instance
- A weather condition sensor (e.g., `sensor.openweathermap_condition`)
- A switch entity controlling the zapper (e.g., `switch.outdoor_plug_2`)
- An `input_boolean` helper to track rain hold

---

### 🛠️ Helper Setup
Create this helper in `configuration.yaml` or via **Settings → Devices & Services → Helpers**:
```yaml
input_boolean:
  bug_zapper_rain_hold:
    name: Bug Zapper Rain Hold
    icon: mdi:weather-rainy
```

---

### 📥 Installation
1. Save the blueprint YAML file as:
```text
config/blueprints/automation/[your_username]/bug_zapper_rain.yaml
```
2. In Home Assistant go to **Settings → Automations & Scenes → Blueprints → Import Blueprint**
3. Choose **"Bug Zapper - Flexible Schedule with Rain Check (v2.0)"**
4. Configure the automation:
   - **Bug Zapper Switch**: Your zapper plug/switch entity
   - **Weather Condition Sensor**: Your weather sensor (e.g., OpenWeather)
   - **Rain Hold Input Boolean**: The `input_boolean.bug_zapper_rain_hold` you created
   - **Turn On Trigger** and **On Time**
   - **Turn Off Trigger** and **Off Time**

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
