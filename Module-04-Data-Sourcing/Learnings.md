# Get the Data – Web Scraping Learnings

--------------------------------------------------

1. Scraping with Excel

Learnings
- Extracted live data from websites directly into Excel using Power Query
- Used Data Tab → Get Data → From Web
- Connected to a website by pasting a URL
- Identified available tables from the webpage

Data Transformation
- Used Query Editor to:
  - Preview data
  - Remove unnecessary columns
  - Transform data before loading
- Understood "Applied Steps":
  - Each transformation is recorded step-by-step

Data Loading
- Loaded cleaned table into Excel
- Used Refresh to fetch updated data from the website

Key Understanding
- Excel can act as a lightweight web scraping tool
- Data remains connected to the original source
- Refresh updates the dataset dynamically
- Transformations are automatically reapplied

Practical Use Case
- Imported Two Week Weather Forecast for Chennai

Applications
- Data analysis
- Visualization
- Dashboard creation
- Trend analysis

--------------------------------------------------

2. Scraping with Python (IMDB)

Learnings
- Introduced web scraping using Python
- Extracted structured data from IMDB

Libraries Used
- requests
- BeautifulSoup
- pandas

Technical Workflow
- Fetched webpage using requests
- Parsed HTML using BeautifulSoup
- Inspected webpage using browser developer tools

HTML Understanding
- Identified:
  - Tag names
  - Class names
  - Nested structure
- Understood hierarchy:
  - Parent containers hold multiple records
  - Child elements store specific values

Data Extraction
- Movie Title → a.text
- Movie Year → span.text
- Rating → strong.text

Data Processing
- Stored extracted data in lists
- Converted lists into pandas DataFrame
- Displayed structured output

Key Understanding
- Webpages are structured using HTML
- Correct tag identification is essential
- Higher-level containers enable bulk extraction
- pandas converts raw data into structured format

Practical Outcome
- Converted IMDB Top Movies list into structured table

Applications
- Data analysis
- Visualization
- Further processing

--------------------------------------------------

3. Wikipedia Data Extraction

Learnings
- Used wikipedia Python library for structured data extraction
- Avoided manual HTML scraping

Concepts Covered
- Installed external libraries using pip
- Used search() to find pages
- Used summary() for concise information
- Limited summary using sentences parameter
- Used page() for full article data

Data Access
- Extracted:
  - URL
  - References
  - Images

Table Extraction
- Used HTML content with pandas.read_html()
- Selected tables using index

Key Understanding
- Wikipedia library simplifies data extraction
- Provides structured access to information
- Tables are stored as lists
- Requires trial-and-error for correct table selection

Practical Outcome
- Extracted structured knowledge data for:
  - Research
  - Data analysis
  - Academic work
  - Automation

--------------------------------------------------

4. Scraping BBC Weather with Python

Learnings
- Extracted structured weather data from BBC Weather

Core Concepts
- Web scraping retrieves HTML content
- requests fetches webpage data
- BeautifulSoup parses HTML
- Browser Inspect tool helps identify structure

Technical Workflow
- Used find_all() to extract multiple elements
- Processed lists to extract required data

Data Cleaning
- Used:
  - String splitting
  - Indexing
  - Regular expressions
- Converted text to numerical values
- Handled special characters (degree symbol)

Data Structuring
- Generated date column using pandas
- Combined lists into DataFrame

Data Export
- Saved output to:
  - CSV
  - Excel

Key Takeaways
- requests → Fetch HTML
- BeautifulSoup → Extract data
- Data cleaning is essential
- Structured datasets enable analysis
- Legal considerations must be followed

Practical Outcome
- Created 14-day weather dataset for Mumbai

Applications
- Data analysis
- Forecast comparison
- Visualization
- Data storage
