# Temperature and Weather Station Data Analysis Near Ann Arbor, Michigan, USA

This project analyzes temperature records and visualizes weather station data in the vicinity of Ann Arbor, Michigan, USA. The goal is to explore historical temperature trends, identify record-breaking events, and map weather station locations for better geographical insights.

## Datasets Used 

- **`temperature.csv`**: Contains temperature data from various weather stations in Ann Arbor over multiple years.
- **`BinSize.csv`**: Contains global weather station data with location coordinates.

---

## Key Considerations
- Each row in the dataset represents a single observation.
- Leap days (February 29th) are removed for consistent visual representation.
- Visualizations include proper legends, labels, and minimal clutter for clarity.

---

## Visualization Considerations
- Clarity: Avoid overcrowding, use appropriate labels and legends.
- Consistency: Ensure uniform data formatting and color schemes.
- Relevance: Only display meaningful information to enhance interpretation.

---

## Project Tasks 

### 1. Plot record high and low temperatures by day (2005-2014) with shaded areas in between.

### 2. Overlay 2015 data points for days when record temperatures were broken.

### 3. Visualize weather stations near Ann Arbor on a map using coordinates.

### 4. Plot a summary of temperature data near Ann Arbor for the year 2015.

---

## Logical Implementation Approach

### Tasks 1 and 2 (Temperature Analysis)
1. Data Cleaning: Remove leap days and ensure data consistency.
2. Aggregation: Compute record highs and lows per day (2005-2014).
3. Overlay 2015 Data: Identify and mark new records.
4. Visualization:
   - Plot high and low records as a shaded graph.
   - Overlay record-breaking 2015 temperatures as scatter points.
   - Add legends, labels, and ensure clarity.
   ### Code and Analysis report can be found in "Tasks 1 & 2.ipynb" file

### Tasks 3 and 4 (Weather Station and 2015 Summary) 
1. Data Filtering:
   - Remove unnecessary columns.
   - Filter relevant weather stations from `BinSize.csv`.
2. Geospatial Filtering:
   - Compute distances from Ann Arbor.
   - Keep only stations within 100 km.
3. Weather Station Map: Plot locations using latitude and longitude.
4. Temperature Summary (2015): Visualize temperature trends for Ann Arbor.
### Code and Analysis report can be found in "Tasks 3 & 4.ipynb" file

---

### Note : Both dataset has been cleaned , organaised and sorted for relevance , the code for which can be found in  "Data Preprocessing.ipynb" file inside Data Preprocessing folder.

---

## Conclusion

The analysis reveals significant climate variability, with 2015 showcasing both record-breaking heat and cold events. These findings align with broader patterns of climate change, indicating a potential shift in seasonal weather patterns. 

---

## Technologies and Modules Used

### 1. Standard Python Modules (No installation required)
- **os**: File and directory path manipulation.
- **datetime**: Parsing, formatting, and manipulating date/time data.

### 2. Third-Party Modules (Require installation via `pip`)
- **pandas**: Data manipulation and CSV handling.
- **matplotlib.pyplot**: Data visualization (line plots, scatter plots, maps).
- **numpy**: Numerical operations and handling NaN values.
- **geopy.distance.geodesic**: Geographic distance calculations (e.g., filtering stations within 100 km).

### 3. Additional Geographic Modules 
- **contextily (ctx)**: Adds basemaps (e.g., OpenStreetMap) to geographic plots.
- **geopandas**: Geographic data manipulation and handling.
- **shapely.geometry.Point**: Creating geometric points from latitude/longitude coordinates.

### Installation Guide
Run the following command to install all required libraries:
```sh
pip install pandas matplotlib numpy contextily geopandas shapely geopy

