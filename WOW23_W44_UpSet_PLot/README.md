# Workout Wednesday Challenge: UpSet Plot in Tableau
**By Albert Lleida, November 2023**

## Challenge Description

I'm a Junior Data Analyst enhancing my visualization skills in Tableau. This is my first time engaging with Workout Wednesdays by Tableau, and this project is the result.

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

![Viz - Albert Lleida](https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/052c360b-b7a8-43b4-b184-b9ad31a46b8f)

This visualization presents the detailed UpSet plot created for the Workout Wednesday challenge. Explore customer purchasing patterns within Furniture sub-categories interactively.

### Development Progress

To solve the main challenges of this project, the information available at [The Information Lab](https://www.theinformationlab.co.uk/2020/01/19/creating-upset-plots-in-tableau/) was tremendously helpful. I've learned about the `FIXED` function in Tableau, which proved vital in solving the cohort customers' challenge.

The `FIXED` function in Tableau allows for calculating an expression using the specified dimensions, irrespective of the other fields in the view. In this challenge, the `FIXED` function enabled the creation of the 'Fixed_CustomerID' calculated field, aggregating customers' sub-category purchases.

Additionally, the article guided me in understanding how to construct the UpSet plot using an index for sorting and setting up the visualization. Employing a CASE statement as an index twice (as dimension and circle), along with a double axis, was pivotal to merge both plots. Overcoming the continuous line challenge was resolved by integrating the 'line dimension' into the mark's path, providing a solution for the consistent line across column dots.

This learning experience allowed me to better grasp Tableau's capabilities and significantly enhanced my visualization techniques.


### Looking Forward

I'm open to feedback and excited to keep honing my Tableau skills. Always learning and improving! 🚀📈

#WOW2023 #WOW2023W44 #Tableau #Visualization #Dashboard
