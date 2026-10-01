<div align="center">

# NEXUS
### Crisis Management Dashboard

**When a smart city's mind is attacked, its operators become its last line of defense.**

![Team](https://img.shields.io/badge/team-SMA--W1-FF751C?style=for-the-badge)
![Type](https://img.shields.io/badge/type-competition--project-13C6D1?style=for-the-badge)
![Stack](https://img.shields.io/badge/stack-HTML%20·%20CSS%20·%20JavaScript-3BD17B?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-FC9E97?style=for-the-badge)

**Team SMA-W1**

</div>

---

## Table of Contents

- [Overview](#overview)
- [The Scenario](#the-scenario)
- [Original Challenge](#original-challenge)
- [Why NEXUS Stands Out](#why-nexus-stands-out)
- [Main Features](#main-features)
- [Pages](#pages)
- [Real-Time Data Engine](#real-time-data-engine)
- [Original Data Examples](#original-data-examples)
- [Design System](#design-system)
- [Technologies](#technologies)
- [Responsive Design](#responsive-design)
- [Team](#team)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Competition Purpose](#competition-purpose)
- [Closing Note](#closing-note)

---

## Read This!

 For the people looking for it, The original source code is <a href="https://github.com/MehrsamMod/SMA-W1_Nexus/releases/tag/Original_Code">here</a>

---

## Overview

**NEXUS** is a front-end crisis management dashboard built for a simulated smart city in the Middle East — a city whose every artery, from traffic signals to power plants, is run by a single artificial intelligence, also named **NEXUS**.

This project imagines the moment that system is compromised, and answers a single design question: *what does an operator need in front of them, in the first sixty seconds of a citywide crisis, to regain control?*

The result is a full-scale operational interface — not a mockup, not a static prototype — built to look, feel, and behave like software a real emergency command center would trust its city to.

---

## The Scenario

The city's central AI — **NEXUS** — governs:

- Traffic lights and intersections
- Power plants and the electrical grid
- Water systems and reservoirs
- Air pollution monitors
- Security cameras
- Thousands of distributed city sensors

Then, a **massive cyberattack** tears through part of the system. In its wake:

- Traffic collapses into gridlock across multiple districts
- Air pollution spikes to critical, health-threatening levels
- Entire districts sit on the edge of blackout
- Sensor data starts arriving **delayed**
- Sensor data starts arriving **corrupted**
- And somewhere in a control room, operators are left with one tool to make sense of it all — this dashboard.

NEXUS isn't just a UI. It's the operator's only window into a city that's fighting to stay online.

---

## Original Challenge

This project is built on top of the official **NEXUS Web Challenge**, which required:

- A fully interactive web application
- JavaScript-based data management
- Simulated real-time data
- City-sector monitoring
- Map-based data visualization
- Traffic monitoring
- Air-quality monitoring
- Power-grid monitoring
- Crisis detection

Every one of those requirements is met in full. But rather than treating the brief as a checklist, our team treated it as a foundation — expanding it into a coherent, believable operational product with its own visual language, narrative logic, and depth of functionality.

**We didn't replace the original challenge. We built the system it was describing.**

---

## Why NEXUS Stands Out

- **A real command-center feel** — not a dashboard template with different labels, but a purpose-built interface shaped around how a crisis actually unfolds.
- **Depth over decoration** — a dedicated login screen plus eight fully realized operational pages, each with its own working logic, not filler screens.
- **Honest data simulation** — sensor values drift and evolve believably over time instead of jumping to random numbers every refresh.
- **A design system with intent** — every color in the palette has a job; red is earned, not decorative.
- **Built for scrutiny** — structured, documented, and organized clearly enough that a judge — or a new developer — can understand the entire system in minutes.
- **Full ownership, not division of labor** — every page in NEXUS was built end-to-end by a single team member, which means every screen was designed, coded, and refined by someone who understood exactly what it needed to do.

---

## Main Features

| Category | Capabilities |
|---|---|
| **Monitoring** | Real-time city monitoring, interactive city map, traffic monitoring, power-grid monitoring, air-quality monitoring, water-system monitoring, security monitoring |
| **Response** | Alerts & incidents management, critical-zone monitoring, severity-based triage |
| **Intelligence** | City-wide analysis, sensor reliability & data-quality monitoring |
| **Experience** | Real-time sensor simulation, fully responsive interface, a live Leaflet/OpenStreetMap city map, interactive charts, filtering and search across every module |

---

## Pages

NEXUS ships as a login screen plus eight linked operator pages (`index.html` → `dashboard.html` → `city-map.html` → `power-grid.html` → `air-quality.html` → `water-system.html` → `security.html` → `alerts.html` → `settings.html`), all sharing one sidebar and one design system. Traffic monitoring and data-quality signals aren't split into pages of their own — they're built directly into the City Map, Dashboard, and Alerts screens, described below.

### Login
Professional NEXUS operator login screen — the operator's entry point into the command system.

### Dashboard
The main city command center, giving an at-a-glance read on the entire city:
- Air Quality, Power Grid, Water System, Metro System and Security stat cards with live sparklines
- City map widget
- Critical Zones
- Live Alerts
- Sensor Feed

### City Map
A live interactive map of the city built on **Leaflet** and real **OpenStreetMap** data (via the Overpass and Nominatim APIs), with independently toggleable layers:
- Traffic
- Power
- Metro
- Security
- Sensors
- Water
- Incidents
- Air

Operators can search any location, drop into a per-neighborhood detail view, and read a live HUD (lat/lon/zoom). Traffic is read from real, live traffic-signal data rather than a simulated grid — the honest limitation being that there is no free, keyless, truly live traffic-*congestion* feed, so congestion state is modeled on top of the real signal layer.

### Power Grid
Includes:
- Live Grid Map
- Power Plants
- Power Distribution
- Grid Health
- Recent Events

### Air Quality
Includes:
- Air Quality Map
- AQI Trend
- Monitored Zones
- Pollutants
- Sensor Status
- Zone Details

### Water System
Includes:
- Water System Overview
- Water System Status
- Water Quality Monitoring
- Water Alarms

### Security
Includes:
- Security camera list and feeds
- KPIs: active alerts, cameras online, critical zones, sensors
- Donut, bar and line activity charts
- Live alerts panel with a movable layers widget

### Alerts & Incidents
The operational heartbeat of the crisis response. Includes:
- City Incident Map
- Incident feed with type, district, time and severity filters
- Incident Details
- Incident Timeline

Severity levels: **Critical** · **High** · **Medium** · **Low**

### Settings
Doubles as the system's reporting and analysis home. Includes:
- Report Center and Report Overview (generated report status, scheduling)
- Analysis Dashboard (activity breakdown by severity)
- Operator/system navigation and preferences

Data quality is surfaced inline rather than on a dedicated page — the Dashboard and City Map both track sensor status (active, delayed, corrupted, offline), so operators can see, and question, the trust behind the numbers without leaving their current view.

---

## Real-Time Data Engine

NEXUS uses JavaScript to simulate real-time sensor data across the entire city. The simulation continuously updates:

- Traffic
- AQI
- Power generation
- Sensor status
- Alerts
- Live feed
- Incident status
- Timestamps

Crucially, the data is engineered to **behave**, not just change. Values drift, trend, and respond the way real infrastructure data would — so the dashboard tells a believable, evolving story of the crisis rather than flashing random noise at the operator.

---

## Original Data Examples

**Traffic:**

```javascript
const trafficMap = [
 [0,0,1,0,0],
 [0,1,1,1,0],
 [0,0,2,0,0],
 [1,1,1,0,0],
 [0,0,0,0,3]
];
```

**Pollution:**

```javascript
const pollutionData = [
 { zone: "A1", aqi: 120 },
 { zone: "B4", aqi: 250 },
 { zone: "C2", aqi: 90 }
];
```

**Power Grid:**

```
North Plant
Status: Active
Power: 82%

South Plant
Status: Critical
Power: 21%
```

---

## Design System

NEXUS's visual identity is built around a single idea: **a command center at night, run by people who cannot afford to misread the screen.** The interface uses:

- Dark, futuristic aesthetic
- Smart-city command-center styling
- Middle Eastern visual identity
- Cybersecurity-inspired elements
- Professional emergency-management UI conventions
- Data-focused, noise-free layouts

**Color Palette**

| Purpose | Hex | Role |
|---|:---:|---|
| Background | `#080A0C` | The near-black base the whole interface breathes in |
| Panels | `#101316` | Elevated surfaces for data and modules |
| Panels (secondary) | `#15191D` | Nested/inset surfaces within panels |
| Borders | `#2A3035` | Quiet structural separation |
| NEXUS Orange | `#FF5A00` | The system's signature — action, identity, focus |
| Cyan | `#00D9D9` | Data, live feeds, and system intelligence |
| Normal | `#18C77A` | Everything operating as expected |
| Warning | `#FFB020` | Something needs attention |
| High | `#FF7A18` | Something needs attention *now* |
| Critical | `#FF3B30` | Reserved — deliberately — for the moments that matter most |

The palette also keeps a purple (`#9B6BFF`) and a blue (`#3B9EFF`) in reserve for secondary data series in charts.

Red is never used decoratively in NEXUS. It is earned only by genuinely critical states, so that when an operator sees it, they know it's real.

---

## Technologies

- HTML5
- CSS3
- JavaScript (vanilla, no framework)
- [Leaflet.js](https://leafletjs.com/) for the interactive map
- Live OpenStreetMap data via the Overpass and Nominatim APIs (no API key required)
- [Chart.js](https://www.chartjs.org/) for charts
- Google Fonts (Inter, JetBrains Mono)
- Responsive CSS
- Simulated real-time data engine for non-geographic metrics

---

## Responsive Design

NEXUS is built to be operated anywhere a crisis might demand it — from a full command-center wall display down to a single tablet in the field. It supports **Desktop**, **Tablet**, and **Mobile** through:

- Responsive grids
- Collapsible navigation
- Responsive charts
- Responsive maps
- Mobile-friendly controls
- Scrollable tables

---

## Team

### Team SMA-W1

NEXUS is built by **Team SMA-W1**, a four-person front-end team that split full ownership of the system across its members rather than dividing work by convenience. Each page below was owned end-to-end by the developer responsible for it — from layout and logic to the data it displays.

| Member | Responsibilities |
|---|---|
| **ELENA ALIMIRZADEHKARGAR** | Login, City Map, Data Quality, Analysis, Air Quality, Alerts & Incidents |
| **MANIYA GHARAYAGHZANDI** | Dashboard, Traffic, Power Grid, Settings, Water System |
| Mehrsam Hosseini | Team Member |
| MOHAMMAD SADEGH ZADEH | Team Member |

**ELENA ALIMIRZADEHKARGAR** and **MANIYA GHARAYAGHZANDI** jointly led:

- Linking the project pages into a single cohesive system
- Project integration
- README documentation

---

## Project Structure

```
SMA-W1_Nexus/
│
├── index.html # Login page
├── dashboard.html # Main command center
├── city-map.html # Interactive city map
├── power-grid.html # Power grid monitoring
├── air-quality.html # Air quality monitoring
├── water-system.html # Water system monitoring
├── security.html # Security monitoring
├── alerts.html # Alerts & incidents
├── settings.html # Settings, reports & analysis
│
├── css/
│ └── style.css # Shared design system + all page styles
│
├── js/
│ ├── data.js # Shared simulated data engine
│ ├── nav.js # Sidebar / navigation
│ ├── icons.js # Icon set
│ ├── utils.js # Shared helpers
│ ├── livemap.js # City map live-data logic
│ ├── alerts.js # Alerts & incidents logic
│ └── air-quality.js # Air quality page logic
│
├── assets/
│ ├── nexus-mark.png
│ └── nexus-mark-white.png
│
├── vendor/
│ ├── leaflet/ # Leaflet.js map library
│ ├── leaflet.heat/ # Leaflet heatmap plugin
│ └── chartjs/ # Chart.js charting library
│
└── README.md
```

---

## How to Run
A. Using the link

  You can run, use and interact with NEXUS using the <a href="https://mehrsammod.github.io/SMA-W1-Nexus">link</a>.

B. Running it locally 

You can run NEXUS locally usiing the steps below:

1. Clone or download the project folder.
2. Open the project folder in a code editor (e.g., VS Code).
3. If a live server is available, run the project through it for the smoothest experience with real-time data simulation.
4. Alternatively, open `index.html` directly in a modern web browser.
5. Also, you run do `python -m http.server 8000` on your terminal (Make sure you have Python installed on your machine).
6. No API key is required — the City Map pulls live geodata from the public OpenStreetMap Overpass and Nominatim APIs, so an internet connection is enough to load it.

---

## Competition Purpose

NEXUS was built to demonstrate command over the full breadth of front-end engineering and product thinking:

- Front-End development
- UI/UX design
- JavaScript programming
- Real-time data simulation
- Data visualization
- Interactive maps
- Crisis management systems
- Smart-city concepts
- Responsive web development

---

## Closing Note

A city under attack doesn't need another pretty screen — it needs a system its operators can trust with their next decision. That's the standard **NEXUS** was designed to meet, and it's the standard **Team SMA-W1** held itself to at every stage of the build: from the first data model to the last pixel of the design system.

<div align="center">

### NEXUS — Command. Monitor. Respond.

**Built by Team SMA-W1**

</div>
