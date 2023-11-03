# Workout Wednesday Challenge: Heat Map with Bathymetry Lines in Tableau
**By Albert Lleida, November 2023**



### Challenge Details

- **Created by** @LukeStanke - WOW23 W20
- **Challenge:** Created a heat map showing sales by month and sub-category and calculated the cumulative percent of total sales for each sub-category, including the addition of lines between adjacent cells with different colors.
- **Level:** Hard

#### Key Features

- **Dataset Source:** '2022.2 SuperStore' Dataset on Data.World.
- **Color coding calculation:** 'ROUND([pct_of_total]*50, -1)'

Find the original challenge description at the [WorkoutWednesday site](https://workout-wednesday.com/2023w20tab/).


### [Tableau Visualization: Heat Map with Bathymetry Lines by Albert Lleida](https://public.tableau.com/app/profile/albert1030/viz/HeatMapwithBathymetryLines-WOW2023W20/Historia1?publish=yes)


<img width="1218" alt="HM_Viz_Albert_Lleida" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/9634f202-e7c7-4033-8163-9e781344af41">


### Development Progress

I approached the challenge by initially creating a HeatMap using the 'Order Date' month for columns and calculated the 'pct_of_total' utilizing the Window Function:

<img width="465" alt="Captura de pantalla 2023-11-03 a las 9 45 14" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/efa10414-8f94-4c4c-b4f4-85e1d562cbd1">


Upon constructing the 'color' scale with the provided function, I encountered challenges continuing to build the lines or retaining the original data labels on the grid. Hence, I decided to explore the guidance presented in the solution section.

### Learnings and Findings

The solution was enlightening in several aspects:

1. Utilization of a barplot to create a Heat Map.
2. Logical filling of cells using 'MIN 1.0' and '0.0' axes.
3. Application of the LOOKUP function and IFNULL for handling null data.
4. Creation of horizontal and vertical lines and their adjustment via 'Edit Table Calculation' to function correctly on the grid:

<img width="553" alt="Captura de pantalla 2023-11-03 a las 9 42 42" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/6cebaf34-f53a-482d-ab49-60f8cd89f314">


### Progress and Future Aspirations

The learning curve in this challenge was substantial, yet there remains much more to explore and assimilate in Tableau's functionalities. I'm enthusiastic about embracing more complex challenges and enhancing my skills further.

#WOW2023 #WOW2023W20 #Tableau #Visualization #Dashboard
