# Visual Design 
The two questions that i will use for the project will be: 
1) Question: How has the demographic composition of the global ranking changed in recent years?
    - Demographics and Gender Gap Analysis
    - Motivation: To verify if the game is becoming socially more inclusive or if it remains structurally dominated by specific demographic groups.
2) Question: Is there a correlation between the average age of a nation's players and its average competitive strength?
   - Generational Clash (Youth vs. Experience)
   - Motivation: To verify if the advent of modern training methods chess engines, online databases disproportionately favors nations with a lower average age compared to those relying on traditional experience.


## Visual Mapping Specification

1) Question: How has the demographic composition of the global ranking changed in recent years?

| Name                                 | D   | F   | D'  | X   | Y   | Z   | T   | R   |  —  | []  | CP                |
| :---                                 | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-:               |
| **% number of player per Gender**    | Q   |     |  Q  |  L  |     |     |     |     |     |     |                   |
| **Gender**                           | N   |     |  N  |     |     |     |     |  C  |     |     |                   |
| **Year**                             | Q   |  sl |  Q  |     |     |     |     |     |     |     |  slider           |
| **Age Range**                        | O   |  sl |  O  |     |  P  |     |     |     |     |     |  slider + click   |

es: https://observablehq.com/@observablehq/plot-state-population-change


2) Question: Is there a correlation between the average age of a nation's players and its average competitive strength?

| Name                                 | D   | F   | D'  |  X  | Y   | Z   | T   | R   |  —  | []  | CP                |
| :---                                 | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-:               |
| **Rank Avg.**                        | O   |     |  O  |     |  P  |     |     |     |     |     |                   |
| **# Player**                         | Q   |     |  Q  |     |     |     |     |  S  |     |     |                   |
| **Year**                             | Q   |  sl |  Q  |     |     |     |     |     |     |     |  slider           |
| **Age Avg.**                         | O   |     |     |  P  |     |     |     |     |     |     |  slider + click   |
| **Country**                          | N   |     |  N  |     |     |     |     |     |     |     |  Text             |
| **Region**                           | N   |     |  N  |     |     |     |     |     |     |     |  Legend           |
