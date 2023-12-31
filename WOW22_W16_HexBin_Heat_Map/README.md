# Chile's Seismic Insights (2010-2023) with Hexbin Maps
**By Albert Lleida, November 2023**

<br>
<div align="center">
<img width="860" alt="Captura de pantalla 2023-11-09 a las 0 15 51" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/272f0d15-50e8-4655-ab3b-70132781a5d6">
<p style="font-size: smaller; font-style: italic;">Colors from www.ColorBrewer.org by Cynthia A. Brewer, Geography, Pennsylvania State University.</p>
</div>

<br>

### Key Features
- Dataset Source: 'Earthquakes_EDA_Data.csv'

<br>

### Overview

This visualization project was inspired by a Workout Wednesday challenge ("Hexbin Map of Rat Sightings in NYC" - [WOW2022 | Week 16](https://workout-wednesday.com/2022w16tab/)) by Sean Miller, introducing me to techniques for using **Hexbin maps**. 

The visual power of Hexbin maps immediately captivated me, and I recognized their potential to provide a fresh perspective on a previous earthquake-related project I'd been working on several months prior. My interest in earthquakes stems from my time in Chile, where I was welcomed by an 8.4 magnitude earthquake in the Coquimbo Region in 2015. My first ever experienced... quite a memorable debut!

<br>

<div align="center">
<img width="860" alt="Captura de pantalla 2023-11-09 a las 0 21 35" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/1dadc453-2cfd-454d-9bc0-c3d3b543f7f8">
</div>

---

### Project Background - Chile's Seismic Insights

The **[Chile's Seismic Insights (2010-2023)](https://github.com/alleida23/Chile_Recent_Earthquakes/)** project aimed to analyze seismic events in Chile. It leveraged web scraping, Python data analysis, and Tableau visualization to explore seismic activity trends, magnitudes, depths, and occurrences based on a dataset from 2010 to the present.

In response to WOW22 W16 map challenge, I improved previous visualizations using new skills, particularly focusing on Hexbin maps. The new Tableau visualization of recent earthquakes in Chile incorporates **HexBin Heat Maps**, Scatter plots, Bar charts, and interactive features, providing deeper insights into seismic activity in Chile.

- <em>Former (left): Tableau Map (1-Month Data, Color Scale: Magnitude )</em>
- <em>Updated (right): Hexbin Heat Map (14-Year Data, Color Scale: Earthquake Count)</em>

<br>

<div align="center">
    <div>
        <img style="width: auto; height: 500px;" alt="Image 1" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/67eccf35-1ec9-4e90-9b93-fb45dd815d6b">
        <img style="width: auto; height: 500px;" alt="Image 2" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/ff0dab36-cbe5-410f-b406-f01c99349d14">
        <p>Tableau Visualization of Chile's Earthquakes with Hexbin Maps: <a href="https://public.tableau.com/app/profile/albert1030/viz/HexBin-ChilesEarthquakes/Historia1?publish=yes">Chile's Earthquakes - Tableau Visualization</a></p>
    </div>
</div>

---

### HexBin Map Development Process:

1. To develop the HexBin Map, a tutorial video by Sean Miller ([Link to Tutorial Video](https://www.youtube.com/watch?v=5aR3EiuFHmQ)) was followed. Main steps included:

    - Structuring the geographical features as separate latitude and longitude fields in Tableau.
    - Assigning the geographical types: Latitude and Longitude, respectively.
      
        <br>

        <div align="center">
        <img width="430" alt="Captura de pantalla 2023-11-09 a las 12 34 02" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/92afdb9f-f644-4fc9-80cd-1dafa4565bbd">
        </div>

        <br>

    - Creating a parameter (commonly named 'Ratio') essential for HexBin maps. The 'Ratio' parameter determines the density and granularity of the hexagons. 'Ratio' parameter is set to an Integer, and an initial recommended value (which can be modified later for better visualization) is typically selected to ensure an optimal visualization experience.
        
    <br>

    <div align="center">
    <img width="430" alt="Captura de pantalla 2023-11-09 a las 12 40 14" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/63dca676-7adf-4dc6-b152-bc3ff0ed8c13">
    </div>

    <br>

    - Utilizing the inbuilt functions HEXBINY(Latitude) and HEXBINX (Longitude) and dividing both by the 'Ratio'.   
    
    <br>

    <div align="center">
    <img width="621" alt="Captura de pantalla 2023-11-09 a las 12 31 28" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/db4c0018-dee4-4ed6-84a0-0ebea4572987">
    <img width="621" alt="Captura de pantalla 2023-11-09 a las 12 30 45" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/e2bc98f6-c4fd-4593-9546-df9460aebc6a">
    </div>
    
    <br>

1. **Importing Hexagon Shape:**
    - Despite having the inbuilt function for HexBin maps, Tableau does not have a hexagon shape among its default features. A hexagon shape was downloaded from [Flaticon](https://www.flaticon.es/) in PNG format.
    
    <br>

    <div align="center">
    <img width="56" alt="Captura de pantalla 2023-11-09 a las 13 28 37" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/0b44fd35-30fe-4fb0-a3db-91564449c0f3">
    </div>
    
    <br>

    - Accessed the 'My Tableau Repository' folder on my computer and added the hexagon shape into the folder "Shapes".
    - Refreshed the Shapes section in Tableau.
    - The same process was repeated for another graph, this time with icons, as observed in the following image:
    
    <br>


    <div align="center">
    <img width="430" alt="Captura de pantalla 2023-11-09 a las 13 24 10" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/0436296e-d791-4791-befc-07fd8d9e8300">
    </div>

    <br>

2. **Importing Color Palette:**
    - Following the instructions provided in the challenge text, the code of 'Preferences.tps' file was edited and copied into the "My Tableau Repository".
    - Tableau was then rebooted, and all colors from the imported palette were added for use in the visualizations.

---

### Final Thoughts

Combining my experiences and new Tableau skills allowed me to revisit the earthquake project with greater insight and visual depth. The Hexbin map challenge significantly contributed to the enhanced representation of seismic data.
