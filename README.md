# 🌡️ GitCool — Urban Heat Island Mitigation Planner

> **See the heat. Simulate the solution. Plan the intervention.**

GitCool is an interactive **Urban Heat Island (UHI) Mitigation Planner** designed to help citizens, planners, and local governments understand where cities are heating up and explore practical ways to cool them down.

Instead of treating urban heat as just a temperature problem, GitCool connects **heat mapping → intervention simulation → citizen action → government planning → health impact** in one interactive interface.

---

## 🚀 What GitCool Does

### 🗺️ 1. Interactive Urban Heat Map

Explore high-risk heat zones across **Delhi NCR and Jaipur** using an interactive map.

* Heat-severity visualization
* Temperature-based zone markers
* Search for cities, localities, and landmarks
* Click directly on the map to generate a heat zone
* Open locations directly in Google Maps
* Switch between street and dark map layers
* View individual zone temperatures and severity levels

Heat zones are classified as:

| Surface Temperature | Severity    |
| ------------------- | ----------- |
| `< 36°C`            | 🟦 Cool     |
| `36–38°C`           | 🟩 Mild     |
| `38–40°C`           | 🟨 Warm     |
| `40–42°C`           | 🟧 Hot      |
| `42–44°C`           | 🟥 Very Hot |
| `> 44°C`            | 🔴 Extreme  |

The prototype currently includes predefined zones in Delhi and Jaipur, including industrial areas, urban centers, green spaces, and **Manipal University Jaipur (MUJ)**.

---

## 🌿 2. Intervention Simulator

Select a heat zone and simulate how different interventions could affect its surface temperature.

### Cooling interventions

* 🌳 New trees
* 🌱 Green roof coverage
* 🛣️ Reflective / cool pavement
* 💧 Water bodies / blue infrastructure
* 🌿 Vertical wall greening

The simulator provides:

* Baseline surface temperature
* Simulated temperature after intervention
* Temperature change
* Estimated AC energy savings
* Before/after heat maps
* Animated visual representation of interventions

The simulator also includes an **Auto-Optimize Zone** feature that generates a sample intervention prescription for a selected zone.

---

## 🔥 3. Explore What Makes Heat Worse

GitCool doesn't only simulate cooling.

A **Heating Mode** allows users to explore the effect of negative urban changes such as:

* Loss of tree cover
* Increased dark pavement
* Additional generators / AC waste heat

This creates a simple **cause → effect** visualization showing how urban development choices can increase heat.

---

## 👥 4. Citizen Action

Urban cooling isn't only a government problem.

GitCool provides practical actions individuals and communities can take, including:

* 🌳 Planting native shade trees
* 🌱 Starting terrace or kitchen gardens
* 🏠 Using reflective roof paint
* ❄️ Using ACs more efficiently

Each action can be expanded to understand how and why it can contribute to local cooling.

---

## 🏛️ 5. Government & Budget Planning

The **Government & Budget** section translates the heat problem into potential municipal-scale projects.

Example interventions include:

| Project                   | Estimated Expense |
| ------------------------- | ----------------: |
| Cool Roof Mission Subsidy |           ₹120 Cr |
| Miyawaki Micro-Forests    |            ₹45 Cr |
| Blue-Green Corridors      |           ₹650 Cr |
| District Cooling Systems  |           ₹385 Cr |

The dashboard also compares a hypothetical **₹1,200 Cr Urban Cooling Mission** against major Indian Union Budget sectors using an interactive Chart.js visualization.

---

## ❤️ 6. Health Impacts

The platform explains why urban heat matters beyond uncomfortable temperatures.

Interactive health topics include:

* Heat stroke & cardiovascular strain
* Extreme heat and wet-bulb conditions
* Disrupted sleep
* Energy poverty and inequality

Each topic contains an expandable explanation connecting urban heat to human health and vulnerable populations.

---

# 🧠 How It Works

At a high level:

```
                 ┌─────────────────┐
                 │   Urban Area    │
                 └────────┬────────┘
                          ↓
                 ┌─────────────────┐
                 │   Heat Mapping  │
                 └────────┬────────┘
                          ↓
                 ┌─────────────────┐
                 │ Identify Hotspot│
                 └────────┬────────┘
                          ↓
                 ┌─────────────────┐
                 │ Intervention    │
                 │   Simulator     │
                 └────────┬────────┘
                          ↓
              ┌───────────┴───────────┐
              ↓                       ↓
      Citizen Actions          Government Planning
              │                       │
              └───────────┬───────────┘
                          ↓
                 ┌─────────────────┐
                 │ Cooler & More   │
                 │ Resilient City  │
                 └─────────────────┘
```

---

# 🛠️ Tech Stack

GitCool is intentionally built as a lightweight browser-based application.

### Frontend

* **HTML5**
* **CSS3**
* **Vanilla JavaScript**

### Visualization & Mapping

* **Leaflet.js** — interactive maps
* **Leaflet.heat** — heatmap visualization
* **Chart.js** — budget visualization

### Mapping / Location Services

* **OpenStreetMap** — map tiles
* **Nominatim** — location search / geocoding
* **Google Maps deep links** — external location navigation

### Design

* Responsive layout
* Interactive dashboards
* Animated intervention visualization
* Dark, thermal-inspired UI

The application loads its mapping, heatmap, charting, and font libraries directly from CDN resources.

---

# ▶️ Running Locally

No build system or package installation is required for the current prototype.

### 1. Clone the repository

```bash
git clone https://github.com/getgud07/gitgud.git
cd gitgud
```

### 2. Open the application

Simply open:

```text
index.html
```

in a modern web browser.

Alternatively, run a simple local server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

> Some map/search functionality depends on external services, so an internet connection is recommended.

---

# 📍 Current Coverage

The current prototype contains predefined heat zones for:

### Delhi NCR

* Mayapuri Industrial Area
* Okhla Industrial Area
* Bawana Industrial Area
* Karol Bagh
* Connaught Place
* Delhi Ridge / Sanjay Van

### Jaipur

* Sitapura Industrial Area
* Walled City / Johari Bazaar
* Manipal University Jaipur
* Mansarovar
* C-Scheme
* Nahargarh Biological Park

The application also supports searching for custom locations and generating custom map zones.

---

# ⚠️ Prototype / Simulation Disclaimer

GitCool is currently a **hackathon prototype**.

The intervention simulator uses simplified mathematical relationships to demonstrate the potential direction and relative impact of different interventions. It should **not** be interpreted as a scientific prediction, engineering specification, or municipal deployment model.

Similarly, searched locations use a prototype heat estimate rather than automatically retrieving authoritative satellite-derived temperature measurements.

A production version would integrate validated datasets such as satellite-derived Land Surface Temperature, local meteorological observations, building footprints, vegetation data, demographics, and validated urban climate models.

---

# 🎯 Vision

Cities are getting hotter, but most people don't have an intuitive way to answer:

> **Where is the heat?**
> **Why is it happening?**
> **What can we change?**
> **How much could it help?**
> **Who should act?**

GitCool aims to turn those questions into an interactive planning workflow.

**Identify → Simulate → Prioritize → Act.**

---

## 🏆 Built for Hackathon

**Project:** Urban Heat Island Mitigation Planner
**Team Name:** GitCool
**Team Members:** Ratnesh Pushp, Abhay Singh Aman, Srijeet Roy, Shubhankar Varshney. 
**Status:** Hackathon Prototype
**Built with:** HTML • CSS • JavaScript • Leaflet • Chart.js

---

## 📄 License

This project is currently a hackathon prototype.
