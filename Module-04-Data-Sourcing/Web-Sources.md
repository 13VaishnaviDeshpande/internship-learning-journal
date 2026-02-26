# Data Sources and Extraction Methods

--------------------------------------------------

1. Time and Date – Weather Forecast

Website
- https://www.timeanddate.com/weather/

Example Used
- Two Week Weather Forecast – Chennai

Type of Data Extracted
- Date
- Temperature
- Weather Conditions
- Wind
- Forecast Information

Method of Extraction
- Excel Power Query
- Data → Get Data → From Web
- Selected "Table 0" from detected tables
- Removed unnecessary columns
- Loaded as refreshable table

Live Data Connection
- Excel file remains connected to the website

Update Methods
- Data → Refresh
- Right click table → Refresh

Key Feature
- Fetches latest forecast data automatically on refresh

--------------------------------------------------

2. IMDB – Top Rated Movies

Website
- https://www.imdb.com/chart/top/

Data Extracted
- Movie Title
- Release Year
- IMDB Rating

Method Used
- Loaded webpage using requests
- Parsed HTML using BeautifulSoup
- Inspected elements using browser developer tools

Data Extraction
- a tag → Title
- span tag → Year
- strong tag → Rating

Data Processing
- Stored data in lists
- Converted into pandas DataFrame

Type of Extraction
- HTML tag-based scraping
- Class-based element selection
- Static web scraping

Nature of Data
- Live website data
- Not auto-refreshable
- Requires re-running Python script for updates

--------------------------------------------------

3. Wikipedia Data Extraction

Website
- https://www.wikipedia.org/

Example Used
- Article search (e.g., IIT Madras)

Data Extracted
- Search results
- Page summaries
- Full article content
- Article URL
- References
- Images
- Tables

Extraction Method
- Used wikipedia Python library
- Avoided manual scraping with requests and BeautifulSoup

Table Extraction
- Retrieved page HTML
- Used pandas.read_html()
- Selected table using index
- Converted into DataFrame

Nature of Data
- Live Wikipedia data
- Requires script re-execution for updates
- Structured access via API-like interface

--------------------------------------------------

4. BBC Weather

Website
- https://www.bbc.com/weather

Example Used
- Mumbai – 14 Day Weather Forecast

Data Extracted
- High Temperature (°C)
- Low Temperature (°C)
- Daily Summary
- Forecast Dates

Extraction Method
- Fetched HTML using requests
- Parsed using BeautifulSoup
- Located elements using:
  - Span tags
  - Specific class names

Data Processing
- Used regular expressions for cleaning text
- Structured into pandas DataFrame

Output
- Saved as CSV file
- Saved as Excel file

Nature of Data
- Live weather data
- Requires script re-execution for updates
- Extracted using HTML tag-based scraping
