# 🏁 Formula 1 Race Simulation & Visual Analytics System

A Python-based motorsport analytics and visualization project that combines race physics modelling, FastF1 telemetry analysis, sector optimisation, and a broadcast-style animated race renderer.

This project simulates and visualizes a complete Formula 1 race environment by integrating:

- Mathematical circuit modelling  
- Real telemetry data (FastF1)  
- Sector speed analytics  
- DRS logic simulation  
- Championship points dynamics  
- High-fidelity race animation  

---

## ▶️ Live Demo / Showcase

📺 Watch Full 4K Broadcast Simulation:  
👉 [https://youtube.com/video-link-here](https://youtu.be/aW4u1AQKxGA?si=eAwlu5RmLDKrLZUJ)


## 🎬 Visual Preview

### 🟢 Pre-Race Grid
![Pre Race](preview/pre_race.png)

### 🏎️ Live Race Broadcast
![Race](preview/race.png)

### 🏁 Post-Race Results
![Post Race](preview/post_race.png)

---

## 📌 Project Overview

Modern Formula 1 analytics relies on interpreting track characteristics, vehicle dynamics, sector performance, and race evolution.

This system reconstructs that pipeline:

1. Builds a Derived Reference Circuit from 24 official tracks  
2. Performs sector speed analysis using FastF1 telemetry  
3. Extracts track centerline via computer vision  
4. Generates waypoints & geometry mapping  
5. Simulates race progress, gaps, and DRS logic  
6. Renders a 4K broadcast-style animated race


## 🚀 Key Features

✅ Derived F1 Reference Circuit  
✅ Sector Speed Analytics (FastF1 Telemetry)  
✅ Telemetry-based Speed Optimisation  
✅ Image-based Track Centerline Extraction  
✅ Race Physics & Gap Simulation  
✅ DRS Detection + Activation Logic  
✅ Championship Points Modelling  
✅ Constructor Standings Animation  
✅ Multi-panel Broadcast UI  
✅ 4K Frame Rendering + FFmpeg Export  

---

## 🧠 System Architecture


### 1️⃣ Circuit Analysis
**01_circuit_analysis.py**

- Aggregates 24 F1 circuits
- Computes:
  - Total calendar distance
  - Corners per km
  - Right-turn bias
  - DRS zones per km
  - Seconds per km
- GenerateDerived Reference Circuitit**
- CalculaSpeed-Class Similarity RankingngCore Concept:t:**  
Statistical synthesis of track characteristics → theoretical reference circuit.

### 2️⃣ Sector Analysis (Telemetry Driven)n)**
**02_sector_analysis.py**

UFastF1 APIF1 API** to load real telemetry data:

- Loads fastest lap per track
- Splits lSector 1 / 2 / 3 2 / 3**
- Computes:
  - Sector times
  - Sector distances
  - Sector speeds
- Compares speeReference Speed SCore Concept:ncept:**  
Telemetry → Sector Speed Modelling → Performance comparison.

### 3️⃣ Track Centerline Extractionaction**
**03_track_analysis.py**

- Loads black & white circuit image
- Applies:
  - Thresholding
  - Binary inversion
  - Skeletonization (skimage.thin)
- Outputs:
track centerlineceCore Concept:e Concept:**  
Computer Vision → Track Geometry Reconstruction

### 4️⃣ Waypoints & Geometry& Geometry**
**05_waypoints_analysis.py**

- Converts centerline → coordinate waypoints
- Computes:
  - Cumulative distance
  - Normal vectors
  - Sector segmentation
  - CoCore Concept:*Core Concept:**  
Discrete track geometry for animation & physics map

### 5️⃣ Race Physics & Timingysics & Timing**
**07_race_time_analysis.py**

- Interpolates race timeline
- Computes:
  - Driver distance progression
  - Lap calculation
  - Gap & interval modelling
  Physics Concepts:*Physics Concepts:**

- Distance → Time gap conversion  
- Lap wrapping  
- Race completion thr

### 6️⃣ DRS Simulation LogicS Simulation Logic**

Implements realistic DRS mechanics:

- Detection Points (DP1 / DP2)
- Sector-specific activation zones
- Eligibility log integration
- Per-driver Core Concept:g

**Core Concept:**  
Conditional race advantage modelling.

---

## 🎥 Final Renderer
**10_final_rendering.py**

A multi-region broadcast-styleRegion 1 — Live Leaderboardn 1 — Live Leaderboard**
- Smooth position transitions
- Gap & interval throttling
- Podium highlight animation
- Lap counterRegion 2 — Track Map**Region 2 — Track Map**
- Sector coloring
- Sector glow effects
- DRS markers + boxes
- Animated starting lights
- Driver Region 3 — Constructor Championshipnstructor Championship**
- Dynamic team ranking
- Smooth bar movement
- Wins & podium stats
- Team logos + connectors

### Region 4 — Racing Strip
- Scrolling track illusion
- Car icons & DRS bars
- Progress visualization
- Driver cards + podium stats
- Points display at car tip

---

## 📊 Data Sources

- FastF1 API → Telemetry & race data  
- CSV Inputs
  - race_time_interpolated.csv
  - track_waypoints.csv
  - drs_eligibility_logfixed.csv

---

## 🛠️ Tech Stack

- Python  
- NumPy / Pandas  
- Matplotlib (Animation Engine)  
- FastF1 (Telemetry)  
- OpenCV / scikit-image (Computer Vision)  
- PIL (Image Processing)  
- FFmpeg (Video Encoding)

---

## 🎯 Outputs

✔ Derived reference circuit parameters  
✔ Sector speed comparisons  
✔ Track centerline extraction  
✔ Race standings evolution  
✔ Constructor championship dynamics  
✔ 4K broadcast-style race animation  

---


