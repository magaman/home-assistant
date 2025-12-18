# 🏠 My Home Assistant Configuration

Welcome to my Home Assistant repository! This is a collection of my personal configurations, custom dashboards, and automation blueprints. My goal is to create a functional, aesthetically pleasing smart home environment.

## 🌤️ Featured Dashboard: Weather Center
The Weather Center is a high-density dashboard designed to give a 360-degree view of local conditions, ranging from real-time lightning tracking to lunar cycles.

### 🧩 Required Frontend Cards
To use my weather dashboard, you will need the following cards installed. Most are available via [HACS](https://hacs.xyz/).

#### **Core Cards (Built-in)**
* **Markdown** (Dynamic headers/info)
* **Entity Card** (Basic sensor data)
* **Weather Forecast** (Standard HA weather display)
* **Clock Card** (Basic Current Time Card)
* **Webpage** (Used for embedding website snipets)

#### **Custom Cards (HACS)**
| Card Name | Description | Source |
| :--- | :--- | :--- |
| **Ring Tile Card** | Visual ring-style sensors | [GitHub Repo](https://github.com/neponn/ring-tile-card) |
| **Hourly Weather** | Detailed hourly bar charts | [GitHub Repo](https://github.com/decompil3d/lovelace-hourly-weather) |
| **Clock Weather** | Integrated time and weather row | [GitHub Repo](https://github.com/pkissling/clock-weather-card) |
| **Lunar Phase** | Moon phase visualization | [GitHub Repo](https://github.com/ngocjohn/lunar-phase-card) |
| **Blitzortung Lightning** | Real-time lightning strike map | [GitHub Repo](https://github.com/timmaurice/lovelace-blitzortung-lightning-card) |

---

## 🏗️ Blueprints
I share my custom blueprints in the `/blueprints` directory. These are designed to be "plug-and-play" for common automation tasks. 
*Check back soon for my latest lighting and notification blueprints!*

---

## 🛠️ Installation & Usage
1.  **Dependencies:** Ensure [HACS](https://hacs.xyz/) is installed on your Home Assistant instance.
2.  **Frontend:** Install all cards listed in the table above via the HACS "Frontend" section.
3.  **Configuration:** * Browse the `/dashboards` folder.
    * Copy the YAML code.
    * In Home Assistant, create a new Dashboard, enter the **Raw Configuration Editor**, and paste the code.
4.  **Entities:** Remember to find and replace my entity names (e.g., `weather.home`) with your specific local entities.

---

## 🤝 Contributions & Feedback
Feel free to open an issue or a pull request if you have suggestions for layout improvements or better automation logic. 

**Happy Automating!**
