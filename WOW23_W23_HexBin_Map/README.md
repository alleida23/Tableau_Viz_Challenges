# WOW23 W11&23 Challenge: The Dual Axis Hex Map Odyssey 
## Preserving Original Colors and Enabling Multi-State Sales Comparison
**by Albert Lleida, November 2023**

<br>

<img width="800" alt="Captura de pantalla 2023-11-10 a las 17 34 46" src="https://github.com/alleida23/Tableau_Viz_Challenges/assets/124719215/5fc7c104-18ce-4ef5-abb5-423b68042b6b">

Tableau visualization of this challenge here [HexBin Map / Multiple State Selection by Albert Lleida](https://public.tableau.com/app/profile/albert1030/viz/WOW23-W11HexBinMapRetainingOriginalColors/Dashboard1).


## Overview:

Welcome to the visualization challenge! In this task, we aim to create a unique hex map that stands out by preserving the original colors even after state selection. This sets it apart from conventional hex maps that often utilize highlighting options.

The challenge is divided into clear and manageable steps, following the insightful solution approach provided by Donna Coles. Donna's detailed steps for Part 1 can be found [here](https://donnacoles.home.blog/2023/03/16/can-you-compare-state-sales-part-1/), and for Part 2 [here](https://donnacoles.home.blog/2023/06/08/can-you-compare-state-sales-part-2/).

**Challenge Details**

- **Created by** @DonnaColes - WOW23 W11 & WOW23 W23
- **Level:** Hard

For more details on the challenge itself, visit [Workout Wednesday Challenge - Week 11 (Part 1)](https://workout-wednesday.com/2023w11tab/) and [Week 23 (Part 2)](https://workout-wednesday.com/2023w23tab/).


<br>

## Viz Challenge - Part 1

**Key Objectives:**

1. **Hex Map Enhancement:** Implement a dual-axis approach to retain original colors when a specific state is selected.

<br>

### Building the Hex Map with Dual Axis for Retaining Original Colors - Part 1

- Utilize provided files: Superstore dataset v2022.4, Hex map template, hexagon shape file, and transparent shape file.
- Implement a dual-axis approach to preserve original colors when a state is selected.
- Link Orders Superstore data to the hex map sheet, associating State/Province with State.
- Configure hex map appearance by adjusting size, color, and filtering out Alaska and Hawaii.
- Add abbreviation labels and align them centrally for clarity.

<br>

### Identifying the Selected State - Part 1

To achieve our goal of creating a hex map that retains its original colors even after state selection, we need to establish a system that recognizes and differentiates the selected state. This involves the creation of key parameters, calculated fields, and actions:

- **Create a parameter 'pSelectedState' (string):** This parameter serves as the backbone of our interactive system, defaulted to an empty string. It captures the state selected by the user upon interaction.

- **Create a calculated field 'Is Selected State':** This field is crucial for identifying the selected state within our dataset. It compares the [State] to [pSelectedState] and returns a True/False value. This calculated field, named `Is_Selected_State`, acts as a trigger for color modifications.

- **Make a dual axis with pSelectedState:** Implementing a dual axis is essential to our approach. By introducing [pSelectedState] on one axis, we create a seamless integration of the selected state into our existing hex map. This allows us to modify colors dynamically without affecting the overall visual consistency.

- **Modify colors based on True/False values:** With the dual axis in place, we can now dynamically adjust colors based on the 'Is Selected State' calculated field. This ensures that the selected state stands out while maintaining the original colors for the rest of the map.

- **Add a filter action:** To enhance the user experience, we incorporate a filter action. This action prevents selected states from fading into the background, ensuring that the hex map remains clear and visually engaging.

By implementing these parameters (`pSelectedState`), calculated fields (`Is_Selected_State`), and actions (`Deselect Map Marks`), we establish a robust system that seamlessly identifies and highlights the selected state on our hex map, fulfilling our objective of retaining original colors throughout the visualization.

<br>

### Adding Interactivity - Part 1

To enhance user engagement and provide a seamless interactive experience, we introduce key components to our dashboard. Each element is carefully named to reflect its purpose in the system:

- **Set up a parameter action 'Set Selected State':** Establish a parameter action named `Set_Selected_State` to trigger the selection of a state on user click. This action dynamically updates the 'pSelectedState' parameter, facilitating real-time interactions.

- **Add calculated fields 'True' and 'False':** Include calculated fields named `True_Field` and `False_Field` to support the dual-axis approach. These fields act as placeholders for coloring and visibility adjustments during state selection.

- **Implement a filter action 'Deselect Map Marks':** Introduce a filter action named `Deselect_Map_Marks` to prevent fading on selection. This action ensures that the hex map remains clear and vibrant even when specific states are interactively chosen.

- **Create 'State for Param' calculated field:** Develop a calculated field named `State_for_Param` designed to assist in unselecting the state. This field plays a crucial role in the reset functionality, allowing users to revert to the original state after selection.

By naming these components strategically, such as `Set_Selected_State`, `True_Field`, `False_Field`, `Deselect_Map_Marks`, and `State_for_Param`, we create a cohesive and intelligible interactive system within our dashboard, elevating the overall user experience.

<br>

### Building Calculations for Other Charts - Part 1

In this phase, we delve into building calculations for additional charts to complement our hex map. Each step is named for clarity and purpose:

- **Create a new sheet 'Sales Overview' with State, Sales, and Country/Region filters:** Develop a new sheet that acts as the foundation for our supplementary charts, focusing on State, Sales, and Country/Region dimensions.

- **Create 'State Label' calculated field:** Introduce a calculated field named `State_Label` that plays a pivotal role in displaying either the selected state or an average label ('Other States (Avg)'). This enhances clarity in visualizations.

- **Create 'Sales To Display' calculated field:** Establish a calculated field named `Sales_To_Display` to determine the value for the sales measure based on the selected state. This field ensures that the sales data is appropriately represented in the subsequent charts.

- **Duplicate the 'Sales Overview' sheet for a bar chart:** Duplicate the 'Sales Overview' sheet, creating a separate sheet for a bar chart. Arrange the bars based on the 'Is Selected State' field, emphasizing the selected state while maintaining overall chart coherence.

- **Build a line chart for sales over time with dynamic coloring:** Develop a line chart on a new sheet, focusing on sales trends over time. Implement dynamic coloring based on the 'Is Selected State' field, allowing users to discern trends for the selected state against others.

By providing these clear and purposeful names, such as 'Sales Overview,' 'State_Label,' 'Sales_To_Display,' and specifying actions like arranging bars based on 'Is Selected State,' we establish an organized and comprehensible structure for our additional charts.

<br>

### Putting It All Together - Part 1

Now, let's integrate all the components into a cohesive and visually appealing dashboard. Each step is named for clarity and purpose:

- **Arrange the bar and line charts on the dashboard:** Create a visually cohesive layout by placing the bar and line charts. This structure ensures a streamlined and organized presentation.

- **Control the visibility of charts using a boolean field 'Show Viz' based on Is Selected State:** Implement a boolean field named `Show_Viz` to control the visibility of charts dynamically. This field, based on the 'Is Selected State' calculation, ensures that the appropriate charts are displayed based on user interactions.

- **Adjust the layout as needed:** Fine-tune the overall layout of the dashboard to optimize visual appeal and user experience. Consider factors such as spacing, font sizes, and chart alignment to create a polished and professional appearance.

By providing these clear and purposeful names, such as 'Show_Viz,' and emphasizing the importance of layout adjustments, we ensure that our dashboard not only functions seamlessly but also delivers an aesthetically pleasing and user-friendly experience.

<br>

## Viz Challenge - Part 2

**Key Objective:**

1. **Extension of Functionality:** Part 2 extends the solution provided in Week 11 by introducing the capability to capture and compare sales data for multiple selected states rather than a single state.

For more details on the challenge itself, visit [Workout Wednesday Challenge - Week 23 (Part 2)](https://workout-wednesday.com/2023w23tab/).

<br>

### Modified Parameter Handling - Part 2:

Instead of a single state, a delimited list of selected states is captured in the `pSelectedState` parameter using the pipe (|) as a separator. The `State for Param` calculation is adjusted to handle multiple states.

### New Calculations - Part 2:

Calculations like `First Selected State` and `Second Selected State` are introduced to identify the first and second states in the list. A new field, `More than 2 Values Selected?`, is created to identify if more than two states are selected.

<br>

### Color and Shape Adjustments - Part 2:

The `State Colour` calculation replaces the `Is Selected State` field on the Color shelf, dynamically setting colors for the map based on the selected states. Shape legends are adjusted to use a transparent shape for 'Other' states.

<br>

### Alert for More than Two States - Part 2:

A new field, `State Reset`, is introduced to reset the view when more than two states are selected. An alert sheet is added, controlled by the `More than 2 Values Selected?` field.

<br>

### Adapting Other Charts - Part 2:

1. **State Label Field Modification:**
   - The `State Label` calculation is adjusted to display the selected state against the relevant row when only one state is selected.
   - When two states are selected, the state names are displayed against the two relevant rows.

2. **Sales To Display Modification:**
   - The `Sales To Display` field is modified to display different sales values based on whether one or two states are selected.

3. **Bar Chart Adjustments:**
   - Sorting is introduced to ensure the first selected state is listed first.
   - An additional state is added for comparison, and NULL values are excluded from display.

4. **Line Chart Adjustments:**
   - Similar adjustments are made to the line chart.

5. **Displaying Additional Charts:**
   - The display of the bar and line charts is controlled by the `Show Viz` field, which is now modified based on `[First Selected State] <> ""`.

<br>

### Chart Title and Instructions - Part 2:

<br>

The `Chart Title` sheet is modified to reflect the changes in selected states. The title and instructions on the dashboard are updated accordingly.

<br>


## Lessons Learned

For a Junior Data Analyst aspiring to level up my visualization skills, this challenge was a valuable opportunity. The intricacies of structuring a dual-axis hex map, as presented by Donna, provided insights beyond my current proficiency. Creating a visual narrative that doesn't compromise on detail requires breaking away from defaults and embracing inventive approaches. This experience emphasized the importance of mastering the art of structure and design to deliver impactful and tailored visualizations for specific business needs.

