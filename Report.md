# Report

## 1. Demographic Composition Analysis

**Question:** "How has the demographic composition of the global ranking changed in recent years?"

The implemented bidirectional bar chart effectively answers this by plotting Male vs. Female percentages on a shared X-axis relative to age groups on the Y-axis.

* **Gender Gap:** The distinct colors (Red and Blue) and the split axis allow users to immediately visualize the disparity between male and female participation.
* **Structural Trends:** By interacting with the year slider, users can observe if the "pyramid" is widening at the bottom or shifting upwards. This directly addresses the motivation to see if the game remains structurally dominated by specific demographic groups.

### Design vs. Implementation

The implementation adheres strictly to the core visual mapping defined in the design:

* **Quantitative Mapping:** The X-axis represents the percentage of players per gender, matching the design choice that length is the most accurate channel for quantitative data.
* **Ordered Mapping:** Age ranges are mapped to the Y-axis, preserving the natural structure that mirrors biological growth.
* **Nominal Mapping:** Gender is distinguished by Color Hue, consistent with the design's reliance on Bertin’s theories for nominal categories.

### Deviations from the Design

* **Automatic Granularity:** In addition to the design's "Age range click", where clicking a bar would trigger a zoom-in to reveal granular distribution, I decided to add code that automatically detects the range width. If the range is smaller than 25 years, it switches the visualization to "Macro" buckets. 
This is done to smooth the user experience; instead of requiring two distinct interaction modes, the slider handles both filtering and granularity, reducing the user's cognitive load.
* **Reset Button:** I decided to add a reset button to make the user return easily to the full view of the 6-100 years.

---

## 2. Generational Clash (Strength vs. Age)

**Question:** "Is there a correlation between the average age of a nation's players and its average competitive strength?"

The implemented bubble chart addresses this by plotting nations on a 2D plane:

* **Correlation:** The X-axis (Average Age) and Y-axis (Average Strength/ELO) allow users to look for diagonal trends. A trend from top-left (strong/young) to bottom-right (weak/old) would confirm the hypothesis regarding modern training methods favoring youth.
* **Magnitude:** The size of the bubbles represents the number of players, allowing users to differentiate between small nations and major chess powers.

### Design vs. Implementation

The core visual channels match the design sketch and specifications almost perfectly:

* **Position:** Age and Strength are mapped to the X and Y axes respectively, utilized as the "best visual channel for Quantitative and ordered data".
* **Size:** The number of players determines the circle radius, weighting the importance of data points as requested.
* **Color:** Regions are mapped to Hue (Tableau10 scheme), adhering to the design constraint of using color for nominal differentiation of continents.

### Deviations from the Design

* **Search Functionality:** I decided to add a search functionality in the visualization. I observed that it was very difficult to select one specific region or country over all those bubbles due to occlusion and small target acquisition issues. The original design only specified region clicking and hover highlights.
* **Background Context:** The visualization shows a large faint background label. I decided to add this feature (inspired by the Gapminder visualization example seen in class) because, while the original design implied tooltips, I thought it would be better to show the name of the country in the background to help the user keep track of the currently inspected country without visual obstruction.