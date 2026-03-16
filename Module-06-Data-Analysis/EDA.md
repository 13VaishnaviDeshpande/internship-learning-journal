# Correlation using Excel

In this module, correlation analysis was carried out on a COVID-19 dataset using Microsoft Excel. The study concentrated on three key variables: new cases, new deaths, and new vaccinations. Prior to the analysis, the Excel Data Analysis ToolPak was activated through the Add-ins menu.

With the Data Analysis option, a correlation matrix was produced to evaluate the relationships among the selected variables. Correlation coefficients range from −1 to +1, representing both the strength and direction of linear relationships.

The results indicated a strong positive correlation between new cases and new deaths, suggesting that increases in infections are associated with increases in fatalities. In contrast, the relationship between new vaccinations and new deaths showed a weak positive correlation. To complement the numerical findings, scatter plots with trendlines were created to visually examine these relationships and reveal underlying patterns.

---

# Regression using Excel

This tutorial demonstrated regression analysis in Microsoft Excel using a cleaned COVID-19 dataset. The Data Analysis ToolPak was used to perform a multiple linear regression. In this model, new deaths served as the dependent variable, while new cases, new tests, new vaccinations (per 1000), and the stringency index were treated as independent variables.

Before executing the regression, selected variables were scaled by dividing them by 1000 to simplify interpretation of coefficients. The regression procedure involved assigning the dependent variable to the Y range and the independent variables to the X range within the Data Analysis → Regression tool.

The resulting output included key statistical measures such as Adjusted R Square, F-test significance, regression coefficients, and P-values. These indicators were used to assess model performance, determine statistical significance, and interpret how each predictor influences the number of deaths.

---

# Forecasting with Excel

This tutorial explored forecasting methods in Excel using linear regression–based functions and time-series techniques. A sample dataset containing individuals’ heights and weights was used to demonstrate prediction capabilities with Excel’s FORECAST or FORECAST.LINEAR functions.

Initially, the data was converted from imperial units to metric units by transforming height from inches to centimeters and weight from pounds to kilograms. A scatter plot was then generated to visualize the relationship between height and weight. Using forecasting functions, Excel predicted unknown values, such as estimating weight for a given height or height for a given weight.

The session also introduced the TREND function, which applies regression across a range and produces multiple predicted values simultaneously. Additionally, a traffic dataset was used to demonstrate time-series forecasting with the FORECAST.ETS function, which accounts for seasonality and recurring patterns.

---

# Outlier Detection with Excel

This tutorial explained how to identify outliers in a dataset using Microsoft Excel. An outlier is an observation that deviates significantly from the rest of the data and may result from measurement error, variability, or unusual events. Detecting outliers is crucial because they can distort statistical results.

Using a COVID-19 dataset, the new cases column was analyzed for extreme values. The process involved calculating the first quartile (Q1), third quartile (Q3), and the interquartile range (IQR). Lower and upper thresholds were then determined using:

Lower Bound = Q1 − 1.5 × IQR  
Upper Bound = Q3 + 1.5 × IQR  

Excel functions such as QUARTILE.EXC were used to compute quartiles, and logical formulas identified values outside the acceptable range. A box-and-whisker plot was created to visually display the distribution and highlight outliers.

---

# Data Analysis with Python

This tutorial introduced programmatic data analysis using Python, primarily through the Pandas library. A credit card transaction dataset stored in Parquet format was examined. The dataset included fields such as transaction ID, date, approval decision, amount, jurisdiction, dispute category, and regional details.

The data was loaded using pandas.read_parquet(). Initial exploration involved reviewing column names, understanding dataset structure, and identifying variables of interest using commands like df.columns.

Subsequent analyses included grouping, pivot tables, correlations, and time-based aggregations. Pivot tables examined dispute patterns across regions, while correlation analysis explored relationships between transaction amounts and approval outcomes. Time-based analysis combined date and time fields to study approval trends across hours and days. Visual tools such as heatmaps were used to uncover temporal patterns in approval rates.

---

# Data Analysis with SQL

This tutorial demonstrated how SQL can be used for data analysis directly within databases, often in combination with Python and Pandas. Since most large datasets are stored in relational databases, SQL is essential for efficient querying.

A database from the Relational Dataset Repository, specifically Stats.StackExchange, was used. It contained interconnected tables such as posts, users, votes, and post history, linked through identifiers like user IDs. This structure illustrates normalization, where data is stored efficiently without redundancy.

Using Python, data was accessed through pd.read_sql() with SQLAlchemy as the connection engine. Queries were written to compute metrics such as total posts, most active users, and user attributes like reputation, views, and age.

Further analysis combined SQL retrieval with Pandas operations, including correlation studies between age and reputation and regression analysis examining how reputation changes with views. Aggregations were often performed directly in SQL to minimize data transfer and improve performance.

---

# Data Analysis with DuckDB

This tutorial introduced modern analytical tools including the Parquet file format and DuckDB. Parquet is a columnar storage format optimized for analytics, offering strong compression, typed storage, and faster performance compared to CSV or JSON.

A large flight dataset was saved in multiple formats to compare size and loading speed. Results showed that Parquet files were significantly smaller and faster to process.

The dataset was analyzed using both Pandas and DuckDB. DuckDB is an in-process analytical database that supports SQL queries directly on files without requiring data import into a traditional database. A computational task involving grouping flights by delay and counting unique routes was performed using both tools. DuckDB completed the operation much faster due to columnar execution, parallelism, and efficient disk handling. The tutorial also showed seamless integration between DuckDB and Pandas DataFrames.

---

# Geospatial Analysis with Excel

This tutorial demonstrated geospatial analysis using Excel alongside tools such as Python, GeoPandas, and GIS software. The case study examined coffee shop coverage in Manhattan to analyze geographic competition between Starbucks and McDonald’s.

Location data for stores, population statistics, and geographic boundary data were combined. GeoPandas was used to merge demographic information with map boundaries. Coverage areas were calculated to determine which store was closest to residents in different locations.

The processed data was visualized using Excel 3D Maps and GIS tools to display population distribution and store proximity. These visualizations helped estimate potential customer bases for each coffee chain.

---

# Geospatial Analysis with Python

This tutorial focused on geospatial analysis in Python for business decision-making, such as selecting locations for new stores. A dataset containing latitude and longitude coordinates of Starbucks and McDonald’s outlets in New York was used.

Coordinates were processed into geographic points, and the Empire State Building served as a reference location. Distances from each store to this landmark were calculated using the geopy library and added as a new dataset column.

Interactive maps were created with the Folium library, using different marker colors for each brand. Additional analysis identified stores within specified distances and determined the nearest and farthest locations relative to the reference point.

---

# Geospatial Analysis with QGIS

This tutorial demonstrated the use of QGIS, a free open-source Geographic Information System, for creating and managing spatial data. The focus was on working with shapefiles and exporting them into formats such as KML.

Existing shapefiles were obtained from repositories like DIVA-GIS and loaded into QGIS. Attribute tables were examined to understand geographic properties such as region names and administrative classifications.

When shapefiles were unavailable, new ones were created manually using digitizing tools. A polygon representing South Sudan was drawn, and attributes like ID and region name were assigned. The shapefile was then exported in SHP and KML formats for use in other mapping tools such as Google Earth.

---

# Network Analysis in Python

This tutorial introduced network analysis using an IMDB dataset of actors and movies. Each actor was represented as a node, and connections (edges) were formed between actors who appeared in the same film.

A movie-actor matrix was constructed to indicate actor participation in each movie. Matrix multiplication with its transpose efficiently calculated how often pairs of actors collaborated.

Using the scikit-network library, this data was converted into a graph structure. Community detection algorithms, including the Louvain method, were applied to identify clusters of actors who frequently worked together, revealing collaboration patterns within the film industry.

---

# Visualizing Machine Learning

This session emphasized the importance of visualizing machine learning models to make complex systems interpretable. Many advanced models, such as neural networks, support vector machines, and random forests, function as “black boxes,” making their decision processes difficult to understand.

Through examples like customer churn prediction and district clustering using census data, the tutorial demonstrated how visualization techniques can clarify model outputs. Methods such as K-means clustering grouped similar regions based on demographic characteristics and displayed them geographically to reveal meaningful patterns.

The concept of moving along the “ladder of abstraction” was highlighted—transforming raw data into summarized visual insights and enabling interactive exploration to better understand model behavior and relationships.
