# Purpose
Roza has a partially completed dashboard that she needs to finish. She has a completed panel for demographic information and now needs to visualize the bacterial data for each volunteer. Specifically, her volunteers should be able to identify the top 10 bacterial species in their belly buttons. That way, if Improbable Beef identifies a species as a candidate to manufacture synthetic beef, Roza's volunteers will be able to identify whether that species is found in their navel.

Deliverable 1: Create a Horizontal Bar Chart
Deliverable 2: Create a Bubble Chart
Deliverable 3: Create a Gauge Chart
Deliverable 4: Customize the Dashboard

# Files
Use the following links to download the Challenge starter codes.

    Bar chart starter code. 
    Bubble chart starter code. 
    Gauge chart starter code.

# Deliverable 1: Create a Horizontal Bar Chart
# Deliverable 1 Instructions
Using your knowledge of JavaScript, Plotly, and D3.js, create a horizontal bar chart to display the top 10 bacterial species (OTUs) when an individual’s ID is selected from the dropdown menu on the webpage. The horizontal bar chart will display the sample_values as the values, the otu_ids as the labels, and the otu_labels as the hover text for the bars on the chart.
Your bar chart should look like the following image:


    In Step 1, we’ve provided the code for the buildCharts(); function that contains the argument sample, which is the sample that is selected from the dropdown menu.
    In Step 2, we’ve provided the code to retrieve the samples.json file using the d3.json().then() method.
    In Step 3, create a variable that has the array for all the samples.
    In Step 4, create a variable that will hold an array that contains all the data from the new sample that is chosen from the dropdown menu. To retrieve the data from the new sample, filter the variable created in Step 3 for the sample id that matches the new sample id chosen from the dropdown menu and passed into the buildCharts() function as the argument.
    In Step 5, create a variable that holds the first sample in the array.
    NOTE
    You can combine Steps 4 and 5 as one line of code, but make sure you use the correct variable name for Step 6 when retrieving the array data.

    In Step 6, create variables that have arrays for otu_ids, otu_labels, and sample_values.

    In Step 7, create the yticks for the bar chart.

    In Steps 8-10, create the trace object, the layout, and Plotly.newPlot() function for the horizontal bar chart.

    In Step 8, create the trace object for the bar chart, where the x values are the sample_values and the hover text for the bars are the otu_labels in descending order.
    In Step 9, create the layout for the bar chart that includes a title.
    In Step 10, use the Plotly.newPlot() function to plot the trace object with the layout.
    After you have completed the coding requirements, your dashboard will look like this image when it loads for the first time:


# Deliverable 1 Requirements


    Code is written to create the arrays when a sample is selected from the dropdown menu.
    # Refer to code: Resources\d3.js
    Code is written to create the trace object in the buildCharts() function, and it contains the following:
        The y values are the otu_ids in descending order
        The x values are the sample_values in descending order
        The hover text is the otu_labels in descending order.
    
    # Refer to Code: JS\charts.js
    
    Code is written to create the layout array in the buildCharts() function that creates a title for the chart.
    
    When the dashboard is first opened in a browser, ID 940’s data should be displayed in the dashboard, and the bar chart has the following:
        The top 10 sample_values are sorted in descending order
        The top 10 sample_values as values
        The otu_ids as the labels

    # Refer to Image: Resources\Images\Deliverable1.PNG
    # Refer to Image: Resources\Images\Deliverable2.PNG

# Deliverable 2: Create a Bubble Chart

Deliverable 2 Instructions
Using your knowledge of JavaScript, Plotly, and D3.js, create a bubble chart that will display the following when an individual’s ID is selected from the dropdown menu webpage:

    The otu_ids as the x-axis values.
    The sample_values as the y-axis values.
    The sample_values as the marker size.
    The otu_ids as the marker colors.
    The otu_labels as the hover-text values.
    Your bubble chart should look like the following image:

      A bubble chart of a selected individual’s OTUs

      Download the BellyButton_bubble_chart_starter_code.js file, copy the starter code from Steps 1-3, and add it to your charts.js file after Step 10 for Deliverable 1.

      Use the variables that were created in Deliverable 1 to populate the bubble chart. Then, use the instructions below to write the code for the trace object, the layout, and Plotly.newPlot() function to create the bubble chart.

      To create the trace object for the bubble chart do the following:
      Assign the otu_ids, sample_values, and otu_labels to the x, y, and text properties, respectively.
      For the mode and marker properties, the mode is "markers" and the marker property is a dictionary that defines the size, color, and colorscale of the markers.
      If you’d like a hint on how to create a trace object for a bubble chart, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.


      To create the layout for the bubble chart, add a title, a label for the x-axis, margins, and the hovermode property. The hovermode should show the text of the bubble on the chart when you hover near that bubble.
      If you’d like a hint on how to create a layout for a bubble chart, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.


      Lastly, use the given Plotly.newPlot() function to plot the trace object and layout.
      After you have completed the coding requirements, your dashboard will look like the image below when it loads for the first time, with the bar chart you created in Deliverable 1 and the bubble chart.

      The Belly Button dashboard with a horizontal bar chart of the top 10 bacteria cultures found and the bubble chart

# Deliverable 2 Requirements


  The code for the trace object in the buildCharts(); function does the following:
        Sets the otu_ids as the x-axis values
        Sets the sample_values as the y-axis values
        Sets the otu_labels as the hover-text values
        Sets the sample_values as the marker size
        Sets the otu_ids as the marker colors
  The code for the layout in the buildCharts(); function does the following:
        Creates a title
        Creates a label for the x-axis
  The text for a bubble is shown when hovered over
  When the dashboard is first opened in a browser, ID 940’s data should be displayed in the dashboard. All three charts should also be working according to their requirements when a sample is selected from the dropdown menu

  # Refer to Code: JS\charts.js
  # Refer to: Resources\Images\Deliverable2.PNG

# Deliverable 3: Create a Gauge Chart
# Deliverable 3 Instructions
    Using your knowledge of JavaScript, Plotly, and D3.js, create a gauge chart that displays the weekly washing frequency's value, and display the value as a measure from 0-10 on the progress bar in the gauge chart when an individual ID is selected from the dropdown menu.

    Your gauge chart should look similar to the following image:

    The gauge chart showing the washing frequency for scrubs per week




    Download the BellyButton_gauge_starter_code.js, using Steps 1-3 in the buildCharts() function initialize variables that hold arrays for the sample that is selected from the dropdown menu on the webpage.

    In Step 1, create a variable that filters the metadata array for an object in the array whose id property matches the ID number passed into buildCharts() function as the argument.
    In Step 2, create a variable that holds the first sample in the array created in Step 2.
    NOTE
    You can combine Steps 1 and 2 as one line of code, but make sure you use the correct variable name for Step 3 when retrieving the washing frequency value.

    In Step 3, create a variable that converts the washing frequency to a floating point number.
    In Step 4, create the trace object for the gauge chart.
    If you’d like a hint on how to create a gauge chart, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.


    In Step 5, create the layout for the gauge chart making sure that it fits in the <div></div> tag for the gauge id.
    In Step 6, use the Plotly.newPlot() function to plot the trace object and the layout.
    After you have completed the coding requirements, your dashboard will look like this image when it loads for the first time, with the bar chart you created in Deliverable 1, the bubble chart created in Deliverable 2, and the gauge chart:

Sample of a completed dashboard

# Deliverable 3 Requirements


    The code to build the gauge chart does the following:
        Creates a title for the chart.
        Creates the ranges for the gauge in increments of two, with a different color for each increment.
        Adds the washing frequency value on the gauge chart.
        The indicator shows the level for the washing frequency on the gauge.
        The gauge is added to the dashboard.
        The gauge fits in the margin of the <div> element.
        When the webpage loads, the bar and bubble chart are working according to the requirements in Deliverable 1 and 2, respectively, and the gauge chart is working according to the requirements listed for this Deliverable

 # Refer to Code: JS\charts.js
# Refer to: Resources\Images\Deliverable3.PNG
        
# Deliverable 4: Customize the Dashboard

    
# Deliverable 4 Requirements
You will earn a perfect score for Deliverable 4 by completing all requirements below:

The webpage has three customizations.
When the dashboard is first opened in a browser, ID 940’s data should be displayed in the dashboard, and all three charts should be working according to the requirements when a sample is selected from the dropdown menu (5 pt)Deliverable 4: Customize the Dashboard 

Deliverable 4 Instructions
Use your knowledge of HTML and Bootstrap to customize the webpage for your dashboard.

Customize your dashboard with three of the following:
Add an image to the jumbotron.
Add background color or a variety of compatible colors to the webpage.
Use a custom font with contrast for the colors.
Add more information about the project as a paragraph on the page.
Add information about what each graph visualizes, either under or next to each graph.
Make the webpage mobile-responsive.
Change the layout of the page.
Add a navigation bar that allows you to select the bar or bubble chart on the page.
When the dashboard is first opened in a browser, ID 940’s data should be displayed in the dashboard, and the three charts should be working according to their requirements.
When a sample is selected, the dashboard should display the data in the panel and all three charts according to their requirements.

# Deliverable 4 Requirements


The webpage has three customizations. 
When the dashboard is first opened in a browser, ID 940’s data should be displayed in the dashboard, and all three charts should be working according to the requirements when a sample is selected from the dropdown menu

# Refer to Code: JS\charts.js
# Refer to Code: Resources\d3.js
# index.html
# Refer to Images: 
    Resources\Images\Deliverable1.1.PNG
    Resources\Images\Deliverable1.PNG
    Resources\Images\Deliverable2.PNG
    Resources\Images\Deliverable3.PNG
    static\images\bacteria.jpg
