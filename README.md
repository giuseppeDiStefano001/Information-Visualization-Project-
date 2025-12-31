# Information Visualization Project Report

## 1. Visualizations Overview

### Visualization 1: Chess Demographics Analysis
**Goal:** Answer the question *"How has the demographic composition of the global ranking changed in recent years?"*

* **Design:** We implemented a **Bi-directional Bar Chart (Population Pyramid)**. This structure immediately highlights the gender imbalance in chess, with females on the left (red) and males on the right (blue).
* **Interactivity:**
    * **Time Slider:** Allows users to observe the evolution of demographics from 2015 to 2024.
    * **Age Zoom:** A dual-handle slider allows filtering specific age ranges (e.g., juniors vs. veterans).
    * **Macro/Micro View:** Clicking on a macro category (e.g., "<18") zooms into the individual years, providing a granular view of that specific generation.

### Visualization 2: Global Chess Strength vs. Age
**Goal:** Answer the question *"Is there a correlation between the average age of a nation's players and its competitive strength?"*

* **Design:** A **Bubble Chart** where:
    * **X-Axis:** Average Age of the country's top players.
    * **Y-Axis:** Average ELO Rating (Strength).
    * **Bubble Size:** Number of active players (Population).
    * **Color:** Region/Continent.
* **Interactivity:**
    * **Animation:** Dragging the year slider animates the bubbles, showing the "rise and fall" of nations over time.
    * **Smart Filtering:** To manage visual clutter (over 100 nations), we implemented an **Interactive Legend** (click to filter by continent) and a **Search Bar** (to find specific countries).
    * **Context on Demand:** Hovering over a bubble highlights it and displays the country name in the background, keeping the view clean.
---

## 2. Evolution from Initial Design

The final implementation evolved significantly from the initial sketches to address technical challenges (cluttering) and improve user experience.

### A. Handling Visual Clutter (Viz 2)
* **Initial Design:** A static scatterplot showing all nations.
* **Problem:** With ~150 nations, the chart was unreadable; labels overlapped, and small nations were indistinguishable.
* **Final Solution:**
    1.  **Data Filtering:** We excluded nations with fewer than 15 active players or extreme rating outliers (<1900 ELO) to focus on statistically significant data.
    2.  **Smart Labels:** Labels are hidden by default for small nations and only appear upon **Hover** or **Search**.
    3.  **Search Functionality:** We added a search box that highlights the queried country and fades out the rest, allowing targeted analysis.

### B. Navigation & Exploration
* **Initial Design:** Simple static charts for different years.
* **Final Solution:** We integrated **noUiSlider** to create a fluid timeline. This transforms the analysis from a static comparison to a dynamic story, allowing the user to see trends (e.g., the aging of a specific national team) unfold organically.

### C. Data Optimization
* **Challenge:** The original dataset was over 100MB, causing slow loading times and browser crashes.
* **Solution:** We pre-processed the data (Python script), filtering out inactive players and low-rated games. This reduced the file size by ~80%, ensuring smooth animations and fast loading times without sacrificing the quality of the analysis for top-tier chess.