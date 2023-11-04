# Workout Wednesday Challenge: Funnel Chart in Tableau
**By Albert Lleida, November 2023**

### Challenge Details

- **Created by** @Donna Coles - WOW23 W5
- **Challenge:** Recreate a funnel chart visualizing a process with sequential stages where values typically decrease. 
- **Level:** Medium

#### Key Features

- **Dataset Source:** [Sales Opportunity Dataset](https://workout-wednesday.com/2023w05tab/)
- **Stages:** Reflect sequential stages with Stage No: 1 (Prospecting) as the first and either 5 (Closed Won) or 6 (Closed Lost) as the last stages.
- **KPIs to Create:** Total value of Sales Opportunities, % value won, % value lost, % value outstanding.
- **Funnel Chart:** Represents the % amount passing through each stage of the pipeline.

Find the original challenge description at the [WorkoutWednesday site](https://workout-wednesday.com/2023w05tab/).

### [Tableau Visualization: Funnel Chart by Albert Lleida](https://public.tableau.com/app/profile/albert1030/viz/WOW23W5-GANTTBARFUNNELCHART_16990492340780/Historia1?publish=yes)

<img width="847" alt="FC_Viz_ALleida" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/3850543c-bd4a-43e8-9484-799802d029c5">


### Development Overview

The development process primarily involved filtering out 'Closed Lost' (Stage No = 6), fixing its value to 'Total Lost', and calculating various required values such as the value for each stage and the accumulated values ordered from the first to the last stage.

![Captura de pantalla 2023-11-04 a las 13 46 12](https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/a5d837f9-fb89-40bc-b83e-8bc10fa3a562)

To calculate 'Stage Lost' and 'Total Amount Passed through Stage', after encountering initial challenges using 'IF INDEX() = 5' for filtering and calculation, switching to 'IF MIN()' resolved the issues when transforming the table to Gantt bars.

<img width="446" alt="Captura de pantalla 2023-11-04 a las 13 43 54" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/d4ea98dc-e6f8-45c1-8788-e480e61e6467">


### Learnings and Findings

Understanding the logic behind 'Position to Plot' and 'Proportion of Total' was instrumental in centering the bars to create the funnel effect, providing valuable insights into effectively displaying funnel charts for process assessment. For further insights, details on resolving challenges and gaining a deeper understanding of this process can be found [here](https://donnacoles.home.blog/2023/02/02/can-you-build-a-funnel-chart/).

![Image](https://donnacoleshome.files.wordpress.com/2023/01/image-81.png?w=1024)
*Credits: Donna Coles*

<img width="298" alt="Captura de pantalla 2023-11-04 a las 13 20 28" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/77b2fa82-8d97-4b8d-8579-efb1784c10c4">

### Progress and Future Aspirations

The completion of the Funnel Chart using Gantt Bars to represent the pipeline was an insightful experience. As a junior data analyst, this method proved particularly useful for assessing processes and stages. Future aspirations involve further exploration of diverse visualization methods and their applications in data analysis.

#WOW2023 #WOW2023W5 #Tableau #Visualization #Dashboard #FunnelChart #Pipeline
