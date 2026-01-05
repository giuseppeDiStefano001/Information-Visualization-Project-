# FIDE Chess Data Visualizations

This project contains two interactive data visualizations based on FIDE chess player datasets. It analyzes the demographic evolution of players and the correlation between a nation's average player age and competitive strength.

## Visualizations Included

1.  **`1_FIDE_ChessDemographics.html`**
    * **Type:** Population Pyramid and Bar Chart.
    * **Description:** Visualizes the gender distribution across different age groups over the last decade.
    * **Features:** Interactive year slider, age range filtering (zoom), and gender split calculation.

2.  **`2_FIDE_GenerationalClash.html`**
    * **Type:** Bubble Chart (Scatter Plot).
    * **Description:** Explores the relationship between a country's average player age and their average ELO rating.
    * **Features:** Time-lapse animation (2015-2024), region filtering, search functionality, and tooltip details.

## Dependencies

This project relies on the following external libraries:
* **[D3.js (v7)](https://d3js.org/)**: Used for data manipulation, SVG rendering, and axis generation.
* **[noUiSlider (v15.7.1)](https://refreshless.com/nouislider/)**: Used for the interactive year and age range sliders.

## Project Structure

The code is configured to load data from a sibling folder named `data` (using the path `../data/filename.tsv`). Please ensure your folder structure looks exactly like this:

```text
/my-chess-project
│
├── data/                      # Folder containing TSV datasets
│   ├── players.tsv
│   ├── players-high-elo.tsv
│   ├── ratings-high-elo.tsv
│   ├── countries.tsv
│   └── iso3.tsv
│
└── viz/                       # Folder containing HTML files
    ├── 1_FIDE_ChessDemographics.html
    └── 2_FIDE_GenerationalClash.html
```
## How to run the visualisations
1. Open your terminal or command prompt.
2. Navigate to the root folder of the project (e.g., /my-chess-project).
3. Run the following command:
    ```text
    Bash
     # For Python 3
     python -m http.server 8000
    ```
4. Open your web browser and go to:
     ```text
    http://localhost:8000/visualizations/1_FIDE_ChessDemographics.html

    http://localhost:8000/visualizations/2_FIDE_GenerationalClash.html
     ```
