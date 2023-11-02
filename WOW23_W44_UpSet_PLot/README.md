# Workout Wednesday Challenge: UpSet Plot in Tableau
**By Albert Lleida, November 2023**

I'm a Junior Data Analyst enhancing my visualization skills in Tableau. This is my first time engaging with Workout Wednesdays, and this project is the result.

### Challenge Details

- **Challenge:** Built an UpSet plot to visualize combinations of customers purchasing from different sub-categories within Furniture.
- **Level:** Advanced - First attempt at such a complex visualization as a Junior Data Analyst.
- **Progress:** Managed to bring it down to just one calculated field for enhanced efficiency.

#### Key Features

- **Dataset Source:** 20222 Superstore Dataset on Data.World.
- **Dashboard Size:** 1200 x 800 px.
- **Custom Calculations:** 1.
- **Features:** Interactive view enabling users to explore sales data based on different customer cohorts.

Find the original challenge description at the [WorkoutWednesday site](https://workout-wednesday.com/2023w44tab).


### [Tableau Visualization: UpSet Plot by Albert Lleida](https://public.tableau.com/app/profile/albert1030/viz/UpSetPlot-WOW2023W44/Historia1?publish=yes)

<img width="1188" alt="Captura de pantalla 2023-11-02 a las 19 53 37" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/ac00583b-95dd-40dc-be34-d275511f55a5">


This visualization presents the detailed UpSet plot created for the Workout Wednesday challenge. Explore customer purchasing patterns within Furniture sub-categories interactively.

### Development Progress

To solve the main challenges of this project, the information available at [The Information Lab](https://www.theinformationlab.co.uk/2020/01/19/creating-upset-plots-in-tableau/) was tremendously helpful. I've learned about the `FIXED` and `MAX` functions in Tableau, which were pivotal in solving the cohort customers' challenge.

<img width="826" alt="Captura de pantalla 2023-11-02 a las 18 35 26" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/5148bda5-2b34-459f-80a2-80a94483adf1">

The `FIXED` function in Tableau allows for creating a level of detail (LOD) calculation to a specific dimension. In this case, I used `FIXED` in conjunction with `MAX` to create the 'Fixed_CustomerID' calculated field.

The `MAX` function helps to return the maximum value of an expression for each group. By combining `MAX` with `IF` statements within the `FIXED` calculation, I aggregated the purchases of customers within the 'Furniture' category for 'Bookcases', 'Tables', 'Chairs', and 'Furnishings'. This generated a concatenated string representing the sub-categories each customer has purchased from within the 'Furniture' category.

The 'Fixed_CustomerID' calculated field in the UpSet plot aggregates these sub-category purchases for each customer, enabling a comprehensive visualization of customer purchasing patterns within the Furniture sub-categories.

Additionally, the article guided me in understanding how to construct the UpSet plot using an index for sorting and setting up the visualization. Employing a CASE statement as an index twice (as dimension and circle), along with a double axis, was pivotal to merge both plots. Overcoming the continuous line challenge was resolved by integrating the 'line dimension' into the mark's path, providing a solution for the consistent line across column dots.

<img width="238" alt="Captura de pantalla 2023-11-02 a las 18 36 32" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/de710cbd-363d-49d1-b74a-b56d4fd996cc">

This learning experience allowed me to better grasp Tableau's capabilities and significantly enhanced my visualization techniques.


### Looking Forward

I'm open to feedback and excited to keep honing my Tableau skills. Always learning and improving! 🚀📈

#WOW2023 #WOW2023W44 #Tableau #Visualization #Dashboard
