# Data Extraction & Web Scraping Projects


--------------------------------------------------

1. Web Scraping Using Excel

Source Type
- Public Website
- Structured HTML Table
- Live Data Connection

Tools Used
- Microsoft Excel
- Power Query (Get & Transform)

Data Source
- Website: https://www.timeanddate.com/weather/
- Example: Two Week Weather Forecast – Chennai

Workflow
- Connected Excel to website using Data → Get Data → From Web
- Extracted structured table data
- Loaded data into Excel as a query
- Transformed data using Power Query Editor
- Removed unnecessary columns
- Created a refreshable data connection

Key Concepts
- Web scraping using Excel
- Query Editor
- Table View vs Web View
- Applied Steps tracking
- Data transformation

Key Feature
- The dataset remains connected to the website
- Using Refresh updates the data automatically

--------------------------------------------------

2. IMDB Data Scraping Using Python

Source Type
- Public Website
- Static HTML Data

Libraries Used
- Python
- requests
- BeautifulSoup (bs4)
- pandas

Objective
- Extract Movie Title, Release Year, and IMDB Rating from IMDB

Workflow

1. Import Libraries
import requests
from bs4 import BeautifulSoup
import pandas as pd

2. Fetch Webpage
response = requests.get(URL)

3. Parse HTML
soup = BeautifulSoup(response.content, "html.parser")

4. Extract Data
- Title: a.text
- Year: span.text
- Rating: strong.text

5. Store Data
- Save into lists
- Convert into pandas DataFrame

Output
- Structured table containing Title, Year, Rating

--------------------------------------------------

3. Data Extraction Using Wikipedia Library

Source Type
- Wikipedia Articles
- Structured and Semi-Structured Data

Libraries Used
- Python
- wikipedia
- pandas

Installation
pip install wikipedia

Objective
- Extract structured data without manual HTML scraping

Functionalities
- Search: wikipedia.search()
- Summary: wikipedia.summary()
- Full Page: wikipedia.page()
- URL: page.url
- Images: page.images
- References: page.references

Table Extraction
import pandas as pd
tables = pd.read_html(page.html())

Advantage
- No manual HTML parsing
- No BeautifulSoup required
- Direct structured data access

--------------------------------------------------

4. BBC Weather Data Scraping

Source Type
- Public Website
- Dynamic Weather Data

Libraries Used
- Python
- requests
- BeautifulSoup
- pandas
- re
- datetime

Objective
- Scrape 14-day weather forecast data for Mumbai

Data Extracted
- High Temperature (°C)
- Low Temperature (°C)
- Weather Summary
- Date

Workflow

1. Fetch Data
requests.get(URL)

2. Parse HTML
BeautifulSoup(response.content, "html.parser")

3. Extract Elements
- High Temp: day-temperature-high
- Low Temp: day-temperature-low
- Summary: span elements

4. Data Cleaning
- Remove unwanted text
- Convert temperature values
- Use regex for formatting

5. Create Date Range
pd.date_range()

6. Save Data
df.to_csv()
df.to_excel()

# References and Resources

--------------------------------------------------

## GitHub Actions
- GitHub Actions Documentation: https://docs.github.com/en/actions
- Workflow Syntax: https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions
- Schedule Event: https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule
- Cron Expression Builder: https://crontab.guru/
- GitHub Status Page: https://www.githubstatus.com/

--------------------------------------------------

## Screen Scraping with Gemini
- Google AI Studio: https://aistudio.google.com/
- Gemini Overview: https://deepmind.google/technologies/gemini/
- Gemini API Documentation: https://ai.google.dev/docs
- Simon Willison (AI & scraping research inspiration): https://simonwillison.net/
- OCR Reference: https://en.wikipedia.org/wiki/Optical_character_recognition
- Multimodal Learning: https://en.wikipedia.org/wiki/Multimodal_learning

--------------------------------------------------

## Microsoft MarkItDown
- Microsoft MarkItDown GitHub Repository: Search "Microsoft MarkItDown GitHub"
- Markdown Guide: https://www.markdownguide.org/
- OpenAI Platform: https://platform.openai.com/
- IBM Docling (Comparison Tool): https://github.com/IBM/docling
- RAG Concept: https://www.pinecone.io/learn/retrieval-augmented-generation/

--------------------------------------------------

## Nominatim – OpenStreetMap
- OpenStreetMap: https://www.openstreetmap.org/
- Nominatim Documentation: https://nominatim.org/
- Geopy Documentation: https://geopy.readthedocs.io/
- OpenStreetMap Licensing: https://www.openstreetmap.org/copyright
- Google Maps Geocoding (Comparison): https://developers.google.com/maps/documentation/geocoding

--------------------------------------------------

## DocSearch Scraping Tutorial

### Primary Website
- Insider Intelligence Archive
- ~369 pages
- ~7000 articles
- Structured content pages
- Used as real-world scraping target for semantic search demo

### Tools Referenced
1. httpx Documentation  
   - HTTP requests  
   - Redirect handling  
   - Timeout management  

2. lxml Documentation  
   - XPath parsing  
   - HTML tree navigation  

3. tqdm Documentation  
   - Progress monitoring in loops  

4. Stack Overflow  
   - Debugging httpx  
   - Redirect issues  
   - XPath troubleshooting  

### LLM Tools Mentioned
- ChatGPT  
- Bing AI  
- Phind  

### Usage
- Generating Python snippets  
- Debugging assistance  
- Research-based answers  

### Concepts Referenced
- Rubber Duck Debugging  
- Ignobel Prize  
- Friday Night Experiments  
- Discovery of Graphene  

### Key Philosophy
- Build fast prototypes  
- Show working demos  
- Use AI as coding copilots  
- Iterate with small correct steps  

--------------------------------------------------

## Scraping PDFs

### Primary Website
- Premier League Publications Page  
- Contains:
  - Seasonal handbooks  
  - Fixtures documents  
  - Competition documentation  
- 25–30 downloadable PDFs  

### Libraries Used
1. BeautifulSoup (bs4)  
   - HTML parsing  
   - Extracting links  

2. tabula  
   - read_pdf()  
   - convert_into()  
   - area parameter  
   - pages parameter  

3. pandas  
   - DataFrame processing  
   - Tabular data handling  

### Key Concepts
- PDF vs HTML scraping  
- File handling in Python  
- Binary file writing  
- Page-specific extraction  
- Region-based table detection  

### Techniques
- HTML parsing  
- String manipulation  
- File I/O  
- Structured data conversion  
- Batch downloading  

--------------------------------------------------

## Vibe Coding

### Documentation
- OpenAI API Docs: https://platform.openai.com/docs
- Python Docs: https://docs.python.org/3/
- FastAPI Docs: https://fastapi.tiangolo.com/
- Requests Docs: https://docs.python-requests.org/
- GitHub Docs: https://docs.github.com/

### Tools Used
- Visual Studio Code: https://code.visualstudio.com/
- Postman: https://www.postman.com/

### Purpose
- API integration  
- Backend development  
- AI-assisted coding workflows  
DocSearch Scraping Tutorial

Files Created

1. scrape2.py
Main Python script used to:
- Iterate through archive pages
- Extract article URLs
- Scrape individual article content
- Save structured output

2. cache2/ (Directory)
- Stores cached HTML responses
- Uses MD5 hash of URLs as filenames
- Prevents repeated downloads during development

3. urls2.txt
- Stores extracted article URLs
- Allows resuming scraping without repeating archive parsing

4. scraped2.json
Final structured output containing:
- title
- body content

5. scraped2.csv (Optional)
- Alternative export using pandas
- Tabular representation of scraped content


Python Libraries Used

1. httpx
- Used instead of requests
- Supports async (if needed later)
- Allows redirect handling
- Used with:
  follow_redirects=True
  raise_for_status()

2. lxml.html
- Used for fast and standards-compliant HTML parsing
- Used XPath expressions for content extraction

3. tqdm
- Displays progress bar while iterating pages

4. hashlib
- Used MD5 hashing for safe cache filenames

5. os
- Directory creation
- File existence checks
- Path handling

6. json
- Saving structured scraped data

7. pandas (optional)
- Exporting results to CSV


Website Scraped

Insider Intelligence archive

- ~369 archive pages
- ~7000 articles scraped

Structure:
Archive pages list article links

Each article page contains:
- Title (H1 with specific class)
- Body content (within structured div containers)


Architecture Flow

1. Loop through archive pages (archive/1 → archive/n)
2. Extract links containing /content/
3. Deduplicate links using set
4. Loop through article URLs
5. Fetch content using cached_get()
6. Parse title and body via XPath
7. Store structured results
8. Save JSON incrementally


Scraping PDFs

Files Created

1. Downloaded PDF Files
Source: Premier League publications webpage

Approximately 25–30 PDF documents stored in:
- Local folder (e.g., ./premier_league/)
- Or Google Drive (if using Colab)

Examples:
- Premier League Handbook 2021-22.pdf
- Premier League 2 Handbook.pdf
- Fixtures PDF
- Season Preview PDFs

2. pl_interactive_combine.pdf
- Selected PDF for table extraction
- Contains ~19 pages
- Page 18 contains final league standings table

3. table_output.csv
- Structured CSV extracted from page 18
- Generated using tabula.convert_into()
- Contains:
  Team name
  Final standings
  Additional parsed table columns


Python Libraries Used (PDF Section)

1. BeautifulSoup (bs4)

Purpose:
- Parse HTML of webpage
- Extract anchor tags
- Filter links ending with ".pdf"

Used with:
- HTML parser
- find_all('a')

2. requests

Purpose:
- Download PDF files
- Write binary content to disk

3. tabula

Purpose:
- Read tables from PDFs
- Convert extracted tables into DataFrame
- Export directly to CSV

Important Functions:
- read_pdf()
- convert_into()

Parameters Used:
- pages=18
- pages="all"
- area=[top, left, bottom, right]
- output_format="csv"

4. pandas (optional)

Purpose:
- Store extracted tables
- Inspect DataFrame before saving


Website Used

Premier League Publications Page

Contains:
- Multiple season handbooks
- Fixtures PDFs
- League documentation


Workflow Architecture

Step 1
Parse webpage using BeautifulSoup

Step 2
Extract all links ending with ".pdf"

Step 3
Generate filename using:
link.split("/")[-1]

Step 4
Download each PDF and store locally

Step 5
Use tabula.read_pdf() to extract tables

Step 6
Refine extraction using:
- Specific page number
- area parameter

Step 7
Convert cleaned table into CSV


Vibe Coding

Files

1. main.py
Core application file where the primary logic of the project was implemented.
Handled:
- user input
- API calls
- output rendering

2. requirements.txt
Contained all required Python dependencies such as:
- requests
- fastapi / flask (for backend handling)
- openai (for AI-assisted coding)
- pandas (for data handling)

3. .env
Stored environment variables such as:
- API keys
- configuration settings

4. README.md
Documented:
- project overview
- setup instructions
- usage steps


APIs Used

1. OpenAI API
Used for:
- AI-assisted code generation
- prompt-based responses
- automation support

2. REST APIs
Demonstrated how to:
- Send GET and POST requests
- Handle JSON responses
- Integrate third-party services into applications

3. GitHub API (Conceptual Demonstration)
Showed how:
- repositories
- commits
- automation workflows
can be managed programmatically


Tools & Platforms

- VS Code
- GitHub
- Postman (for API testing)
- Python
- AI coding assistants

