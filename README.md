# README for Interactive US State Connections Visualization (Temporal Sankey Diagram)

## Overview
This script visualizes connections between US states based on specified data using GeoPandas, Matplotlib, and ipywidgets. It plots the centroids of US states and displays the connections between them based on the 'magnitude' attribute for a given year.

## Requirements
- GeoPandas
- Matplotlib
- Pandas
- ipywidgets

## Data Files
- US States GeoJSON: 'https://raw.githubusercontent.com/PublicaMundi/MappingAPI/master/data/geojson/us-states.json'
- Connection Data CSV: Custom file path (example: '/path/to/connection_data.csv')

## Features
- Interactive year slider to change the displayed data for different years.
- Normalized color mapping to represent connection magnitudes.
- Visualization of US states with centroids and boundary lines.

## Usage
1. **Data Preparation**: 
    - Reads US states data from a GeoJSON file.
    - Preprocesses the geometry data and reprojects it to 'EPSG:3395' CRS.
    - Calculates centroids for each state.
    - Reads connection data from a CSV file and creates a dictionary mapping connections to their magnitudes.

2. **Interactive Visualization**:
    - Utilizes an interactive slider to select the year.
    - Updates the plot based on the selected year.
    - Visualizes connections using lines with colors and thickness representing the magnitude of connections.
    - Includes a color bar to indicate the scale of connection magnitudes.

3. **Display**:
    - Creates a VBox layout with the plot and the interactive slider for user interaction.

## Running the Script
To run the script, ensure all required libraries are installed and execute the script in a Jupyter Notebook environment. The interactive plot should display within the notebook.

## Note
The script expects a specific format for the connection data CSV. Ensure the CSV has columns 'state1', 'state2', 'Year', and 'magnitude'.
