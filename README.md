# Data Analysis Projects
---------------------------------------------------------------------------------------------------------------------------
A collection containing a variety of R programming assignments and data projects completed as part of undergraduate coursework in environmental data science, geospatial science and R programming courses. Includes analysis that reference a variety of RStudio packages and that cover the scope of multiple different areas such as emissions data, species populations and resource usage. I also include an array of ArcGIS Pro projects that utilize geospatial data to display trends and map patterns in land use, energy data and campsite locations.
---------------------------------------------------------------------------------------------------------------------------
## About
**Author:** Joachim Vogl  
**Institution:** Colorado State University  
**Major:** Environmental Science | **Minor:** Statistics

-----------------------------------------------------------------------------------------------------------------------
## Projects ##
---------------------------------------------------------------------------------------------------------------------------
- ## Project Skills Summary
- Data wrangling, manipulation, and visualization with `tidyverse` and `ggplot2`
- Exploratory data analysis, summary statistics, and outlier detection
- Probability simulation and reproducibility using `set.seed()` and random sampling
- Statistical inference including t-tests, ANOVA, correlation, and linear regression
- Multivariate analysis and assumption testing (Levene's, Shapiro-Wilk, Tukey HSD)
- Spatial data analysis and GIS visualization using `sf` and `tmap`
- Time series analysis and future value prediction using linear regression models
- Custom function development, for-loops, and iterative sampling
- Working with real-world environmental, ecological, and economic datasets
- R Markdown for reproducible research and professional report generation
- Data cleaning including NA handling, type conversion, and column reordering

-----------------------------------------------------------------------------------------------------------------------

### Renewable Energy Usage - Cartographic Design Project
Choropleth map layout visualizing renewable energy usage (%) by country for 2022 using data from Our World in Data joined to a Natural Earth countries layer. Practiced tabular joins, graduated color symbology, normalization for choropleth mapping, unique value classification, and cartographic effects including hatching and gradient fills. Produced a multi-frame map layout with three projections — one world view and two continent-level insets — each displayed in a projection appropriate for that area of interest. Applied definition queries, city labels for major world cities filtered by population threshold, and exported a final polished PDF layout meeting journal-style cartographic standards.

**Tools:** ArcGIS Pro, Natural Earth Data, Our World in Data

**Source:** Natural Earth Data (countries layer), Our World in Data (renewable energy % by country, 2022)

---------------------------------------------------------------------------------------------------------------------------

### Grand Teton National Park Raster Suitability Campsites Analysis
Binary and weighted raster suitability analysis to identify ideal group campsite locations along the Teton Crest Trail using ArcGIS Pro and ModelBuilder. Downloaded and projected a USGS 1/3 arc-second DEM, then derived Slope and Viewshed rasters using the Slope and Visibility tools. Implemented a binary overlay by reclassifying inputs to 1/0 suitability values and combining with Map Algebra, using a trail buffer as a spatial mask. Implemented a weighted overlay using Distance Accumulation on the trail, reclassifying all three inputs to a 1–4 suitability scale, and applying a weighted Map Algebra expression: (Slope × .45) + (Distance × .3) + (Views × .25). Compared binary vs. weighted approaches and produced a final multi-frame map layout with inset maps showing highest suitability areas, extent indicators, and a summary of suitable area by value and acreage.

**Tools:** ArcGIS Pro, ModelBuilder, USGS National Map, Spatial Analyst

**Source:** USGS National Map — 1/3 Arc-Second Digital Elevation Model (DEM), downloaded January 2025. Trail and peaks data provided via NR319 course lab data package.

---------------------------------------------------------------------------------------------------------------------------

### Vector Suitability Analysis — Black-Footed Ferret Reintroduction
Multi-criteria vector suitability analysis using ArcGIS Pro ModelBuilder to identify suitable reintroduction sites for black-footed ferrets in Weld and Larimer Counties, Colorado. Acquired and prepared spatial data from the Colorado Geospatial Data Portal, USGS National Map, and Colorado Parks and Wildlife. Built an automated geoprocessing workflow using tools including Buffer, Clip, Select by Location, Select by Attribute, Union, Intersect, and Erase. Reclassified and overlaid four criteria layers: road proximity, municipal proximity, public land ownership, prairie dog colony potential to produce final suitable area outputs. Summarized results by land ownership type using Summary Statistics. Replicated the full model on a second county by modifying and re-running the ModelBuilder workflow. Produced professional map figures with locator maps, scale bars, and captions following cartographic best practices.

**Tools:** ArcGIS Pro, ModelBuilder, ArcGIS Online, Colorado Geospatial Data Portal, USGS National Map

**Source:** Colorado Geospatial Data Portal (counties, municipal boundaries), USGS National Map (roads), Colorado Parks and Wildlife (prairie dog colony potential), COMAP Generalized 2020 (land ownership via ArcGIS Online)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Vehicle Emissions & Fuel Efficiency Analysis
Exploratory data analysis and visualization of the `mpg` dataset using `ggplot2` and `tidyverse`. Investigates the relationship between engine displacement and highway fuel efficiency across vehicle classes. Includes scatter plots, trend lines, and custom styling.

**Tools:** R, ggplot2, tidyverse, palmerpenguins

**Source:** EPA fuel economy dataset 

-----------------------------------------------------------------------------------------------------------------------

### NCAR-NEON Ecosystem Flux Data Analysis

Analysis of ecosystem gross primary productivity (GPP) data from NEON flux towers and CLM simulations, examining seasonal patterns, site-level differences, and temporal trends in carbon uptake.

**Tools:**
- Language: R
- Libraries: tidyverse, readxl, lubridate
- Functions: select(), mutate(), filter(), group_by(), 
             summarize(), ggplot2, if_else(), everything()

**Source:** National Ecological Observatory Network (NEON) flux towers & NCAR Community Land Model (CLM) simulations

-----------------------------------------------------------------------------------------------------------------------

### Crab Morphology - Multivariate Statistical Analysis

Tests Bergmann's rule using fiddler crab carapace width data from 
13 coastal salt marsh sites, examining relationships between organism 
size, latitude, and temperature variables.

**Tools:** 
- Language: R
- Libraries: tidyverse, lterdatasampler, car
- Functions: aov(), TukeyHSD(), lm(), leveneTest(), 
             cor(), ggplot2, geom_boxplot(), geom_smooth()

## Key Findings
- Significant size differences among sites (F(2,83) = 60.02, p < 0.001)
- Crab size increases with latitude, supporting Bergmann's rule
- Water temperature variation alone does not predict crab size (p = 0.528)
- Latitude is the strongest predictor of carapace width (β = 0.559, p < 0.001)

**Source:** Johnson (2019) - Fiddler crab body size in salt marshes 
           from Florida to Massachusetts via lterdatasampler package

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Salaries Dataset — Exploration & Subsetting
Initial exploration of a global data science salaries dataset. Covers loading CSVs, inspecting data dimensions, subsetting rows and columns, and using dplyr's glimpse() function to understand dataset structure.

**Tools:** R, dplyr

**Source:** salaries dataset file

---------------------------------------------------------------------------------------------------------------------------
### Salaries Dataset — Summary Statistics
Deeper analysis of the data science salaries dataset. Extracts salary and experience level columns, computes mean, median, and standard deviation, and uses the table() function to examine frequency distributions across experience levels.

**Tools:** R, dplyr

**Source:** salaries dataset file

-----------------------------------------------------------------------------------------------------------------------

### Data Science Visualization & Salaries Analysis
Exploratory analysis of a dataset of global data science salaries. Examines salary distributions by experience level using boxplots, histograms, and bar charts. Computes summary statistics including mean, median, standard deviation, and quantiles.

**Tools:** R, base graphics

**Source:** salaries dataset file

-----------------------------------------------------------------------------------------------------------------------

### Probability & Simulation
Introduction to probability and reproducibility in R. Covers random sampling, coin flip simulation, seed-setting for reproducible results, and random number generation using `rnorm()`.

**Tools:** R, base stats

**Source:** internal R coin data

-----------------------------------------------------------------------------------------------------------------------

### Sampling Statistics & Heart Rate Data
Statistical analysis of a heart attack patient dataset. Focuses on sampling distributions, maximum heart rate data extraction, and calculating sampling statistics.

**Tools:** R, base stats

**Source:** Heart attack patient dataset (heart.csv) - project data

-----------------------------------------------------------------------------------------------------------------------

### Random Walk Simulation
Spatial simulation of a random walk across 10,000 steps using a matrix of (x, y) coordinates and directional sampling. Demonstrates matrix operations and simulation logic in R.

**Tools:** R, base graphics

**Source:** R Studio

-----------------------------------------------------------------------------------------------------------------------

### Honey Production Analysis, Sampling
	
Dataset tracking honey production across US states including colony numbers, yield per colony, production volume, stocks, average price, and value of production from 2010 onward.

**Tools:**
- Language: R
- Libraries: Base R only
- Functions: hist(), sample(), rep(), for loops, set.seed()

**Source:** USDA National Agricultural Statistics Service (NASS) honey production data — publicly available

-----------------------------------------------------------------------------------------------------------------------

### NHL Hockey Draft Player Analysis

Exploratory data analysis of NHL draft data examining player performance metrics, demographics, and penalty behavior across positions and nationalities. analysis includes:
- Summary statistics (mean, median, SD) for games played, distribution visualization via boxplots
- Categorical analysis of player positions and nationalities
- Relationship analysis between games played and penalty minutes
- Individual player performance benchmarking
- Outlier detection using IQR method

Key Visualizations:
- Boxplot: Games played distribution
- Barplots: Position and nationality frequency
- Scatterplot: Games played vs penalty minutes
- Grouped boxplot: Penalty minutes by position

**Tools:**
- Language: R
- Libraries: Base R only
- Functions: boxplot(), barplot(), plot(), quantile(), boxplot.stats()

**Source:** NHL Draft dataset - project data

-----------------------------------------------------------------------------------------------------------------------

### Spotify Top Tracks Analysis

Exploratory analysis of Spotify streaming data examining relationships 
between song characteristics including streams, beats per minute, 
modes, and musical keys.

**Tools:**
- Language: R
- Libraries: Base R only
- Functions: boxplot(), barplot(), plot(), boxplot.stats(), table()

**Source:** Spotify Top Tracks dataset — public streaming data

-----------------------------------------------------------------------------------------------------------------------
