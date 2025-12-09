# US Housing Price Analysis Dashboard

## Project Overview
![House](/housing_video_demo.gif)

An interactive Power BI dashboard analyzing the relationship between US home values and socioeconomic variables at the state level from 2005 to 2023.

## Data Source

**Input**: CSV file containing state-level time-series data

**Structure**:
- **Geographic**: 50 US states
- **Temporal**: Annual data points (2005-2023)
- **Variables**:
  - Home Value (primary metric)
  - Remote Work %
  - Income Growth
  - Median Age
  - Median Household Income
  - Population
  - Poverty Rate

## Data Transformation

**Power Query Steps**:
1. **Data Import**: Loaded CSV with proper data types
2. **Date Formatting**: Converted date columns to datetime format
3. **Unpivoting**: Transformed wide format to long format for variable flexibility
4. **Calculated Columns**: Created derived metrics for year-over-year changes
5. **Aggregations**: Built state and national level summaries
6. **Relationships**: Established links between fact tables and dimension tables

## Dashboard Visuals

### 1. Region Selector (Card Visual)
- Displays currently selected geographic region
- Default: "United States"

### 2. US Choropleth Map
- **Type**: Filled map
- **Data**: Most recent values for selected variable
- **Color Scale**: Green (low) to Orange (high)
- **Interaction**: Click states to filter other visuals

### 3. Home Value Trend (Line Chart)
- **X-Axis**: Date (2005-2023)
- **Y-Axis**: Home Value (millions)
- **Color**: Yellow line
- **Tooltip**: Shows exact values on hover

### 4. Variable Trend (Line Chart)
- **X-Axis**: Date (synchronized with home value chart)
- **Y-Axis**: Selected variable value
- **Color**: Dynamic based on selected variable
- **Purpose**: Enable visual correlation analysis

### 5. Variable Selection Buttons (Slicers)
- Six toggle buttons for variable switching
- Active selection highlighted in green
- Updates map and bottom chart dynamically

## Key Insights

1. **Post-2008 Recovery**: Home values bottomed around 2012 (~$10M) and have grown ~90% to reach ~$19M by 2023

2. **Remote Work Impact**: Remote work remained stable at ~250 for a decade, then spiked 3.4x to ~850 during 2020-2021, coinciding with accelerated home price growth

3. **Regional Variation**: The map reveals significant state-level differences in variable adoption/values, with coastal and tech-hub states showing higher remote work percentages

4. **Pandemic Effect**: The 2020-2023 period shows the steepest home value appreciation, potentially linked to remote work flexibility and changing location preferences

## Use Cases

### Real Estate Professionals
- Identify markets with favorable demographic and economic conditions
- Understand pricing trends and forecast future appreciation
- Compare state-level performance

### Investment Analysts
- Evaluate correlation between socioeconomic factors and home values
- Assess market risks (poverty rate, income stagnation)
- Identify emerging opportunities

### Policy Makers
- Study housing affordability challenges across states
- Understand demographic drivers of housing demand
- Design data-driven housing policies

### Researchers
- Analyze pandemic's impact on housing markets
- Study remote work's influence on real estate
- Examine income-to-housing-value relationships

## How to Use

1. **Select a variable** using the buttons on the right panel
2. **View the trend** in the bottom chart alongside home values
3. **Examine geographic distribution** on the map
4. **Click a state** on the map to filter all visuals to that state
5. **Hover over charts** for detailed tooltips with exact values
6. **Compare patterns** between home values and selected variables to identify correlations

## Technical Details

**Tools**: Power BI Desktop  
**Data Refresh**: Manual (CSV import)  
**File Size**: Optimized for web sharing  
**Compatibility**: Power BI Service, Power BI Mobile