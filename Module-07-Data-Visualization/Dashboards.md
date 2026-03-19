# Data Visualization Notes (Advanced)

---

## Visualising Forecasts with Excel

### Pivot Table Base
- Structures time-series data efficiently.
- Organizes securities against time (dates).
- Enables quick aggregation and filtering.

### Trend Column
- Created using Sparklines.
- Provides compact visualization of trends per security.
- Useful for quick comparative analysis.

### Average Calculation
- Formula: `=AVERAGE(range)`
- Measures central tendency of data.

### Forecasting
- Formula: `=GROWTH(known_y’s, known_x’s, new_x)`
- Estimates future values based on exponential growth trends.

### Daily Growth Percentage
- Formula: `(Forecast - Last Value) / Last Value`
- Indicates expected percentage change.

### Variance (Volatility)
- Formula: `=STDEV(range) / AVERAGE(range)`
- Measures relative variability.
- Useful for risk assessment.

### Range (Optional)
- Formula: `(MAX - MIN) / MIN`
- Alternative measure of dispersion.

### Correlation Analysis
- Formula: `=CORREL(array1, array2)`
- Measures strength and direction of relationships.

### Correlation Matrix
- Built using:
  - Data Analysis ToolPak, or
  - Multiple CORREL formulas
- Displays pairwise relationships across all variables.

### Dashboard Insights
- Identify high-growth opportunities.
- Detect highly volatile securities.
- Analyze strong and weak correlations.

---

## Visualising Animated Data with PowerPoint

### Data Preparation
- Source data (e.g., Wikipedia or datasets).
- Clean using:
  - Paste Special (Values only)
  - Remove formatting and non-essential elements
- Structure data as:
  - Year | Rank | Category | Value

### Data Transformation
- Transpose for correct layout.
- Normalize values for consistent scaling.
- Standardize naming conventions.

### Pivot Table Validation
- Ensures accuracy of rankings and values.
- Helps verify transformations.

### Dashboard Design
- Use shapes to simulate bars.
- Adjust widths proportional to values.
- Include:
  - Labels
  - Values
  - Titles

### Animation
- Use **Morph Transition** for smooth changes.
- Maintain consistent object naming via Selection Pane.
- Recommended naming format: `!!CategoryName`

### Dynamic Effects
- Bars adjust size dynamically.
- New entries animate into view.
- Exiting elements move out smoothly.

### Optimization
- Maintain consistent scaling across slides.
- Use short animation durations (0.5–1 sec).
- Align elements for visual clarity.

### Dashboard Insights
- Tracks ranking evolution over time.
- Highlights emerging and declining entities.
- Supports strong narrative storytelling.

---

## Visualising Animated Data with Flourish

### Animation Principles
- Animation should enhance clarity, not distract.
- Focus on meaningful transitions.

### Object Constancy
- Maintain consistent representation of data points.
- Ensures smooth tracking across frames.

### Animation Controls

#### Line Chart Race
- Animation Duration → speed between data points
- Mode Duration → transition smoothness

#### Bar Chart Race
- Timeline Duration → total animation length
- Movement Speed → bar transition fluidity

#### Line/Bar/Pie Templates
- Controls:
  - Drawing speed
  - Morph transitions
- Option to disable animation when unnecessary

#### Scatter Plot Animation
- Requires unique identifier (Name field)
- Supports:
  - Duration
  - Staggered movement

### Time Controls
- Time slider manages step progression.
- Independent from animation speed.

### Advanced Features
- Entry and exit animations
- Stagger effects for readability
- Handling of consistent/inconsistent series names

### Dashboard Insights
- Proper animation improves comprehension.
- Enhances storytelling and comparisons.
- Prevents misinterpretation when used correctly.

---

## Visualising Network Data with Kumu

### Data Preparation
- Extract from datasets (e.g., IMDB).
- Filter:
  - Relevant categories (movies only)
  - Specific regions if required

### Entity Mapping
- Assign unique IDs to entities.
- Map IDs to readable labels.

### Matrix Construction
- Build Movie × Actor matrix:
  - 1 → presence
  - 0 → absence

### Co-occurrence Matrix
- Multiply matrix with its transpose.
- Interpretation:
  - Diagonal → total participation
  - Off-diagonal → shared occurrences

### Sparse Matrix Optimization
- Use CSR (Compressed Sparse Row) format.
- Stores only non-zero values.
- Improves efficiency.

### Data Formatting
- Convert to edge list:
  - Source
  - Target
  - Weight

### Filtering
- Apply thresholds:
  - Minimum activity per node
  - Minimum connection strength

### Visualization
- Import into Kumu.
- Features:
  - Interactive exploration
  - Node highlighting
  - Cluster detection

### Dashboard Insights
- Identifies central (hub) nodes.
- Reveals clusters and communities.
- Shows indirect relationship paths.

---

## Data Visualisation with Seaborn

### Setup
- Required libraries:
  - numpy
  - pandas
  - matplotlib
  - seaborn

### Data Handling
- Load via pandas or seaborn datasets.
- Clean and preprocess before visualization.

### Distribution Analysis
- `distplot` → histogram + KDE (deprecated, use histplot/kdeplot)
- `kdeplot` → density estimation
- `jointplot` → bivariate analysis
- `pairplot` → multi-variable relationships

### Categorical Analysis
- `barplot` → aggregated values
- `countplot` → frequency
- `boxplot` → distribution and outliers
- `violinplot` → density + distribution
- `stripplot` / `swarmplot` → point-level visualization

### Matrix Visualization
- `heatmap` → correlations
- `clustermap` → hierarchical clustering

### Grid Systems
- `PairGrid` → customizable layouts
- `FacetGrid` → category-based splits

### Regression Analysis
- `lmplot` → regression modeling
- Supports grouping and faceting

### Styling
- `set_style` → themes
- `set_context` → scaling
- Color palettes and despine options

### Dashboard Insights
- Enables deep exploratory analysis.
- Reveals distributions, trends, and relationships.
- Supports statistical storytelling.

---

## Google Charts

### Tools and Integration
- JavaScript-based visualization library.
- Integrates with:
  - Web applications
  - R (via googleVis)
  - Dashboards

### Features

#### Interactivity
- Tooltips
- Filters
- Zooming

#### Customization
- Multiple chart types
- HTML tooltips
- Flexible styling

#### Dashboard Composition
- Combine multiple charts
- Build interactive dashboards

### Motion Charts
- Time-based animation
- Multi-variable encoding:
  - Axes
  - Size
  - Color

### Sankey Diagrams
- Visualize flow between stages.
- Link width represents magnitude.

### Limitations
- Requires internet connectivity.
- Less suitable for static reports.

### Dashboard Insights
- Enhances user interaction.
- Ideal for exploratory analysis.
- Effective for storytelling.

---

## Google Data Studio (Looker Studio)

### Data Setup
- Use structured data sources.
- Ensure:
  - No merged cells
  - Consistent formats
  - Proper headers

### Core Concepts

#### Dimensions vs Metrics
- Dimensions → categorical variables
- Metrics → numerical values

#### Aggregations
- SUM, AVG, MEDIAN, MIN, MAX, COUNT

### Dashboard Features

#### Tables
- Sorting and filtering
- Aggregated summaries
- Heatmap-style tables

#### Filters
- Date range controls
- Dropdown selectors
- Page-level and chart-level filters

#### Interactivity
- Dynamic updates across charts
- Drill-down capabilities
- Click-based filtering

#### Charts
- Bar → comparisons
- Line → trends
- Treemap → hierarchy
- Geo map → location analysis

#### Scorecards
- KPI display
- Period comparison
- Change indicators

#### Styling
- Themes and layouts
- Typography and color control
- Structured sections

### Dashboard Insights
- Enables real-time monitoring.
- Combines multiple perspectives.
- Supports data-driven decision-making.

---

## Summary
- Excel → structured analysis and forecasting  
- PowerPoint → animated storytelling  
- Flourish → advanced interactive animation  
- Kumu → network and relationship analysis  
- Seaborn → statistical visualization and EDA  
- Google Charts → web-based interactivity  
- Looker Studio → dashboarding and reporting  
