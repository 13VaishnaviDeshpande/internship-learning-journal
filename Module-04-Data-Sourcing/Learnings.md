# Module 4 – Learnings

---

# Get the Data – Scraping with Excel

## Learnings
This session introduced how to extract live data from websites directly into Excel using the Power Query feature.

### I learned how to:
- Import web data using:
  - **Data Tab → Get Data → From Web**
- Paste a website URL to establish a connection
- Identify available tables from a webpage
- Use the **Query Editor** to:
  - Preview data
  - Remove unnecessary columns
  - Transform data before loading
- Understand the **Applied Steps** section
  - Each transformation is recorded step-by-step
- Load the cleaned table into Excel
- Refresh the data to fetch updated values from the website

### Key Understanding
- Excel can act as a **lightweight web scraping tool**
- Data remains connected to the original source
- Refresh updates the dataset dynamically
- Transformations are stored and automatically reapplied during refresh

### Practical Use Case
Imported: **Two Week Weather Forecast for Chennai**

This data can now be:
- Analyzed
- Visualized
- Used for dashboards
- Used for trend analysis

---

# Get the Data – Scraping with Python

## What I Learned
This session introduced web scraping using Python to extract structured data from IMDB.

### I learned how to:
Import essential Python libraries:

- `requests`
- `BeautifulSoup`
- `pandas`

Steps performed:

1. Fetch webpage content using `requests`
2. Parse HTML using `BeautifulSoup`
3. Inspect webpage elements to identify:
   - Tag names
   - Class names
   - Nested structure

### Understand HTML hierarchy
- Higher-level containers hold multiple records
- Lower-level tags hold specific data

### Extract data using:

- `a.text` → Movie title  
- `span.text` → Movie year  
- `strong.text` → Rating  

### Data Processing
- Store extracted data in lists
- Convert lists into a **pandas DataFrame**
- Display structured tabular output

### Key Understanding
- Web pages are structured using HTML tags
- Scraping requires identifying correct parent and child tags
- Using higher-level containers allows extraction of multiple records
- `pandas` helps convert unstructured scraped data into structured format

### Practical Outcome
Successfully converted **IMDB Top Movies list** into a clean table format for:

- Data analysis
- Visualization
- Further processing

---

# Get the Data – Wikipedia

## What I Learned
This session introduced the use of the **Wikipedia Python library** to extract structured data directly from Wikipedia.

Instead of manually scraping HTML, the library provides built-in functions to access:

- Search results
- Page summaries
- Full article content
- References
- Images
- URLs
- Tables

### Concepts Understood

Install external Python libraries using:

```bash
pip install wikipedia
```

### Functions Used

Search for pages:

```
search()
```

Retrieve summaries:

```
summary()
```

Limit summary length:

```
sentences parameter
```

Retrieve full article details:

```
page()
```

Access page attributes:

- `.url`
- `.references`
- `.images`

Extract tables using:

- HTML content
- `pandas.read_html()`

### Key Understanding
- Wikipedia library abstracts HTML complexity
- Provides structured access to knowledge data
- Tables on Wikipedia are stored as lists
- Trial-and-error may be required to select the correct table index

### Practical Outcome
Efficiently extracted structured knowledge data for:

- Research
- Data analysis
- Academic projects
- Automation tasks

---

# Get the Data – Scrape BBC Weather with Python

## What I Learned
This session focused on scraping structured weather data from the **BBC Weather website** using Python.

### Key Concepts Understood
- Web scraping involves extracting raw HTML from websites
- `requests` fetches HTML content from web servers
- `BeautifulSoup` parses HTML and allows element extraction

### Browser Inspect Tool Helps Identify
- Tag names
- Class names
- Element hierarchy

### Technical Learnings

Use `find_all()` to retrieve multiple elements.

Clean unwanted text using:

- String splitting
- Indexing
- Regular expressions

Other steps:

- Convert extracted text into numerical format
- Handle special characters like degree symbols
- Generate date column dynamically using pandas
- Combine lists into a structured DataFrame
- Export results to CSV and Excel formats

### Key Takeaways

- `requests` → Fetches HTML  
- `BeautifulSoup` → Extracts information from HTML  
- Data cleaning is essential during scraping  
- Scraped data can be structured and stored for analysis  
- Legal considerations must be checked before scraping

### Practical Outcome
Created a **clean 14-day weather forecast dataset for Mumbai**, ready for:

- Data analysis
- Forecast comparison
- Visualization
- Storage for future processing

---

# GitHub Actions – Scheduling & Automation

## Core Learning
GitHub Actions allows automation of workflows based on events such as:

- push
- pull request
- schedule (cron)

### Key Concepts Learned

- Workflows must be inside `.github/workflows/`
- YAML syntax defines jobs and triggers
- Cron expressions define time-based execution
- All schedules run in **UTC timezone**
- GitHub does **NOT guarantee exact execution timing**

### Cron Structure

```
Minute Hour Day Month Day-of-week
```

Example:

```
*/5 * * * *
```

Runs every **5 minutes**

### Important Insight
Even if scheduled every 5 minutes, GitHub may delay execution due to internal queueing.

Scheduled workflows should **not be used for real-time monitoring**.

### Practical Applications

- Automated deployments
- Dependency scanning
- Security checks
- Monthly reports
- Periodic backups

### Major Takeaway
Automation is powerful but must account for execution delays.

---

# Screen Scraping with Gemini – Vision-Based Data Extraction

## Core Learning
Instead of scraping HTML using BeautifulSoup or Selenium, screen content can be recorded and analyzed by a multimodal LLM.

### Technical Insights

- Recording **1 frame per second** converts each second into an image
- Gemini processes videos as sequential frames
- Each frame costs tokens (~250 tokens per image)
- JSON mode should be enabled for structured output
- Method relies on **computer vision instead of DOM parsing**

### Cost Efficiency
Even **1000 frames cost only a few cents**.

### Advantages
- Works on dynamic websites
- Bypasses HTML complexity
- Handles JavaScript-rendered content
- No browser automation required

### Limitations
- Depends on visible content
- Fast scrolling may skip information
- Not ideal for high-speed scraping

### Major Insight
Vision-based extraction using AI can sometimes replace traditional scraping logic.

Shift observed:

**Code-based automation → Vision-based automation**

---

# Microsoft MarkItDown – Document Standardization for LLMs

## Core Learning
MarkItDown converts multiple file formats into **clean Markdown**, making documents suitable for LLM pipelines.

### Why Markdown
- Lightweight
- Human-readable
- Platform-independent
- Easy for embedding chunking
- Ideal for RAG pipelines

### Modes of Operation

**Without LLM**
- Direct parsing
- Fast conversion
- Suitable for structured PDFs

**With LLM**
- Enables OCR
- Understands layout
- Improves formatting quality

### Applications
- Preparing enterprise documents
- Cleaning PDFs
- Knowledge base preparation
- Dataset generation
- RAG system pipelines

### Major Takeaway
Unstructured data must be standardized before feeding into AI systems.

---

# Nominatim – Geocoding with OpenStreetMap

## Core Learning
Geocoding converts text-based location names into structured geographic data.

Example:

```
"IIT Madras" → Latitude, Longitude, Full Address
```

### Key Technical Points

- Powered by **OpenStreetMap**
- `geopy` acts as Python wrapper
- `user_agent` parameter is mandatory
- Returns structured JSON data
- Includes class and type categorization

### Extractable Data

- Latitude
- Longitude
- Display name
- Bounding box
- Class (tourism, amenity, etc.)
- Type (university, attraction, hospital)

### Applications

- Mapping applications
- Location analytics
- Delivery systems
- Geo-tagging datasets
- Urban planning

### Major Takeaway
Unstructured address text → **Structured geographic intelligence**

---

# OVERALL TECHNICAL INSIGHTS FROM ALL SESSIONS

- Automation (GitHub Actions) enables scheduled DevOps workflows
- Vision-based scraping reduces dependency on traditional HTML parsing
- Document conversion to Markdown improves LLM processing
- Geocoding enables spatial intelligence
- Structured outputs (JSON / Markdown) enable scalable AI systems
- Data preprocessing strongly impacts AI/ML performance

---

# DocSearch Scraping Tutorial

## 1. Semantic Search vs Keyword Search

Keyword search → matches exact words  
Semantic search → uses embeddings to understand meaning

Scraped data enabled building a **semantic proof-of-concept search engine**.

---

## 2. Caching is Critical During Development

`cached_get()` pattern:

- Saves HTML responses locally
- Prevents repeated downloads
- Speeds up debugging
- Allows safe interruption and resume

Core idea:

```
If cache exists → load
Else → fetch → save → return
```

Principle:

**Laziness, impatience, and hubris are programmer virtues**

---

## 3. Scraping Strategy

Stages:

1. Get archive page URLs
2. Extract article links
3. Deduplicate links
4. Fetch article pages
5. Parse structured content
6. Store structured output

Small correct steps > Big complex logic

---

## 4. XPath > Guesswork

Use browser DevTools:

- Inspect elements
- Identify stable container divs
- Avoid sidebars and popups
- Use `contains()` in XPath
- Expect trial and error

---

## 5. Debugging Techniques

### Print Liberally
Print variables frequently.

### Use Breakpoints
Use `breakpoint()` or debugger.

### Rubber Ducking
Explain the problem clearly.

---

## 6. Use LLMs Properly

Two modes:

- Implementation questions
- Troubleshooting strategy questions

Best practices:

- Be specific
- Mention libraries
- Ask for readable code

---

## 7. Proof of Concept > Presentation

A working demo:

- Converts clients faster
- Demonstrates capability
- Enables faster production deployment

**Portfolio > Certificates**

---

## 8. Save Incrementally

Write JSON output inside loops.

Benefits:

- Inspect progress early
- Avoid losing hours of scraping
- Enable modular development

---

## 9. Handle Edge Cases

Expect:

- Redirects
- Empty responses
- Class name mismatches
- Deduplication issues

Real-world scraping requires resilience.

---

# Scraping PDFs

## Extracting PDFs from Webpages

- Use BeautifulSoup to parse HTML
- Extract anchor tags
- Filter links ending in `.pdf`
- Generate filenames using:

```
link.split("/")[-1]
```

Automates downloading multiple PDFs.

---

## Reading Tables from PDFs

Use **Tabula**

Example parameters:

```
pages=18
pages="all"
```

---

## Problem: Extra Content

Tabula may detect multiple sections incorrectly.

Example:

Newcastle United **"125 years"** text mistakenly extracted.

---

## Solution: Area Parameter

```
area=[top, left, bottom, right]
```

Restricts extraction region for cleaner tables.

---

## Direct CSV Conversion

Use:

```
convert_into()
```

Benefits:

- Direct CSV export
- Faster pipeline

---

# Vibe Coding

## Core Concepts Learned

- Idea-first development
- Rapid prototyping
- AI-assisted coding
- Effective prompt engineering

## Technical Learnings

- API integration in Python
- JSON handling
- Secure API key storage
- Project structuring
- Debugging AI-generated code

## Practical Skills Gained

- Product-oriented thinking
- Modular problem solving
- Faster development workflows
- Writing maintainable code

## Overall Outcome

The workshop improved confidence in building applications rapidly using modern development practices.

AI enhances productivity, but **logical thinking and structured problem solving remain essential**.
