# Data Visualization Notes

---

## Visualising Forecasts with Excel

### Time Series Visualization
- Line charts and Sparklines track data over time.
- Helps identify:
  - Trends (upward/downward)
  - Seasonality
  - Fluctuations

### Sparklines
- Path: `Insert → Sparklines → Line`
- Mini charts inside a single cell.
- Useful for:
  - Quick comparisons
  - Dashboard summaries

### Scatter Plot
- Shows relationship between two variables.
- Helps identify:
  - Correlation
  - Outliers
  - Clusters

### Trendline
- Added to scatter plots.
- Types:
  - Linear
  - Exponential
  - Logarithmic
- Shows:
  - Equation
  - R² value

### Conditional Formatting
- Uses color scales to highlight:
  - High/low values
  - Variance
  - Correlation strength

### Key Insights
- Indices often move together.
- Some currencies show high volatility.
- Visuals reveal hidden patterns.

---

## Visualising Animated Data with PowerPoint

### Bar Chart Race
- Animated ranking over time.
- Used for:
  - GDP
  - Market trends
  - Population

### Features
- Dynamic comparisons
- Smooth transitions
- Storytelling approach

### Required Data
- Year
- Category
- Value
- Rank (optional)

### Key Insights
- Shows growth trends
- Highlights ranking changes
- Emphasizes gaps

---

## Visualising Animated Data with Flourish

### Purpose
- Enhances storytelling
- Improves engagement

### Chart Types

#### Line Chart Race
- Dynamic trend visualization
- Adjustable animation speed

#### Bar Chart Race
- Ranking evolution
- Timeline-based animation

#### Story Mode
- Morph between charts
- Maintains object consistency

#### Scatter Animation
- Tracks movement over time
- Requires unique identifier

#### Other Charts
- Heatmaps (fade/flip)
- Radar (animated drawing)
- Hierarchical charts

### Key Insight
- Animation improves understanding of change.

---

## Visualising Network Data with Kumu

### Network Graphs
- Nodes → entities
- Edges → relationships

### Features
- Edge weight = strength
- Clusters = communities

### Connections
- Direct → immediate link
- Indirect → through intermediaries

### Key Insights
- Hubs = highly connected nodes
- Clusters show groups
- Paths show indirect links

---

## Data Visualisation with Seaborn

### Distribution Plots
- Histogram
- KDE
- Rug plot

### Joint Plots
- Scatter
- Regression
- KDE
- Hex

### Pair Plots
- Multi-variable relationships
- Diagonal → distribution
- Off-diagonal → comparison

### Categorical Plots
- Bar → aggregated values
- Count → frequency
- Box → spread & outliers
- Violin → density + distribution
- Strip/Swarm → scatter

### Matrix Plots
- Heatmap → correlation
- Cluster map → grouped patterns

### Regression Plots
- Shows trends with prediction

### Grid Plots
- PairGrid
- FacetGrid

### Key Insights
- Combines statistics with visualization
- Ideal for EDA

---

## Google Charts

### Overview
- JavaScript-based visualization library

### Chart Types
- Bar, Line, Pie, Area
- Geo Maps
- Motion Charts
- Sankey Diagrams

### Sankey Diagram
- Flow visualization
- Link width = magnitude

### Motion Chart
- Animated bubble chart
- Shows:
  - X-axis
  - Y-axis
  - Size
  - Color

### Features
- Tooltips
- Filters
- Animation

### Key Insights
- Interactive and dynamic
- Good for web dashboards

---

## Google Data Studio (Looker Studio)

### Overview
- Dashboard and reporting tool

### Components
- Data Source
- Connector
- Report
- Explorer

### Chart Types
- Tables
- Scorecards
- Line/Bar charts
- Treemaps
- Geo maps
- Heatmaps

### Features
- Sorting and filtering
- Aggregation
- Drill-down

### Key Insights
- Combines multiple visuals
- Supports decision-making

---

## Summary
- Excel → basic and quick analysis  
- PowerPoint → storytelling with animation  
- Flourish → advanced animated visuals  
- Kumu → network relationships  
- Seaborn → statistical visualization  
- Google Charts → web-based interactive charts  
- Looker Studio → dashboards and reporting
  
-------

# Data Visualization & Storytelling Techniques

## Actor Network Visualization
- Represent actor relationships as graphs  
- Nodes = actors, Edges = collaborations  
- Helps visualize:
  - Connections between entities  
  - Paths and relationships  
  - Degrees of separation  
- Useful for network analysis in large datasets  

---

## RAWGraphs
- Supports complex visualizations:
  - Network graphs  
  - Scatter plots  
  - Multi-dimensional charts  
- Built on D3.js  
- Maps dataset dimensions → visual variables  
- Export formats:
  - Vector (SVG)  
  - Raster (PNG)  
- Ideal for quick and flexible data visualization  

---

## Data Storytelling
- Charts communicate insights visually  
- Enables faster understanding of patterns  
- Reduces reliance on long textual explanations  
- Focus on:
  - Clarity  
  - Trends  
  - Key insights  

---

## Interactive Notebooks (Marimo)
- Auto-updating visualizations based on input changes  
- Supports:
  - Sliders  
  - UI controls  
  - Interactive elements  
- Enables dynamic plots  
  - Example: sine wave reacting to parameter changes  
- Combines:
  - Code  
  - Visualization  
  - Real-time data exploration  

---

## Narratives with Excel
- Uses charts for storytelling:
  - Histograms  
  - Line charts  
- Trendlines (linear regression) reveal data direction  
- Features:
  - Dynamic updates via filters  
  - Chart titles linked to cells  
- Charts act as the visual backbone of narratives  

---

## Narratives with Comics
- Uses comic-style visuals instead of traditional charts  
- Key elements:
  - Speech bubbles → insights  
  - Characters → data representation  
  - Expressions → reflect trends  
    - High values → positive expressions  
    - Low values → negative expressions  
- Built using:
  - Image URLs in Google Sheets  
- Provides a creative alternative to standard visualizations  

---

## Summary
- Graphs → relationships and networks  
- Charts → trends and insights  
- Interactive tools → dynamic exploration  
- Comics → engaging storytelling  
