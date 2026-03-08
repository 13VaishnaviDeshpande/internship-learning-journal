# Excel Data Cleaning

## Text Transformations
1. Removed unnecessary suffixes such as "[more]" by using the Find & Replace feature.
2. Applied the TRIM() function to eliminate unwanted spaces within text values.

## Structural Transformations
1. Deleted rows containing blank values in key columns.
2. Eliminated duplicate country entries so that only unique records remained.

## Data Type Transformations
1. Converted columns containing numbers from "General" format to "Number".
2. Adjusted decimal formatting to maintain consistent precision across the dataset.

## Data Quality Improvements
1. Standardized inconsistent text formats.
2. Ensured numeric fields were interpreted correctly.
3. Reduced redundancy within the dataset.
4. Removed incomplete or partially filled records.

---

# Data Transformation in Excel

## 1. Ratio Calculations

### A. Metro Area vs City Area Ratio
- Formula used:
```
=G2/D2
```
- Purpose: Evaluate how large the metropolitan area is compared to the city limits.
- Example insight: Tokyo’s metropolitan region is roughly six times the size of its city boundary.
- Missing metro area values resulted in calculation errors for some rows.

---

### B. Metro Population vs City Population Ratio
- Formula used:
```
=F2/C2
```
- Purpose: Measure the difference between metropolitan population and core city population.
- Example insight: Tokyo produced a ratio close to 2.76.
- Values were filled automatically using Excel’s AutoFill feature.

---

### C. Density Comparison (Crowding Indicator)
- Calculated using the relationship between:
  - Metro Area / City Area
  - Metro Population / City Population
- This helps estimate differences in population concentration between city centers and metropolitan regions.

---

## 2. Pivot Table Transformations

### Creating the Pivot Table
1. Highlight the entire dataset.
2. Navigate to Insert → Pivot Table.
3. Create the pivot table in a new worksheet.

---

### A. Aggregation by Country
- Added **Country** to the Rows section.
- Inserted **Country** again in the Values section as **Count**.
- This revealed how often each country appeared in the dataset.
  - Example: China appeared about 20 times.
  - Angola appeared only once.

---

### B. City-Level Aggregation
- Placed **City** under the Country row grouping.
- Added **City Proper Population** to the Values section.
- Set the aggregation to **Sum**.
- This displayed both individual city population and total population by country.

---

## 3. Chart-Based Insights
1. Created a bar chart from the pivot table results.
2. Applied filters to analyze specific countries such as China and the United States.
3. Observed outliers:
   - Chongqing and Shanghai showed extremely high population values in China.
   - Los Angeles showed high density ratios within the United States.

---

# Text to Columns in Excel

## Structural Transformations
1. Converted raw text stored in a single column into multiple structured columns.
2. Extracted different categorical variables from combined strings.

---

## Delimiter-Based Transformations
Different delimiters were used to separate the data:

1. "(" separated the **Senator Name**.
2. "-" extracted the **Political Party**.
3. ")" extracted the **State**.
4. "," separated the **Vote Status**.

---

## Data Structuring
1. Converted messy web-scraped text into a structured tabular format.
2. Created appropriate column headers.
3. Removed extra columns generated during the splitting process.

---

## Analytical Readiness
1. Converted raw text data into a structured dataset similar to CSV format.
2. Enabled filtering, sorting, and aggregation.
3. Prepared the dataset for further analysis and visualization.

---

# Data Aggregation in Excel

## 1. Weekly Aggregation using Pivot Table

Objective:
- Calculate the sum of **New Cases**
- Group results by **Country and Week**
- Separate results by **Year (2020 and 2021)**

### Pivot Configuration
- Rows → Location (Country)
- Columns → Week
- Values → Sum of New Cases
- Filter/Grouping → Year

Insight:
This arrangement revealed weekly COVID case trends across different countries.

---

## 2. Monthly Aggregation using Pivot Table

Objective:
- Aggregate new cases by month and country.

### Pivot Configuration
- Rows → Year → Month
- Columns → Location
- Values → Sum of New Cases

Insight:
The pivot table highlighted monthly waves of COVID infections.

---

## 3. Color Scales (Conditional Formatting)

Purpose:
Highlight regions with high or low numbers of cases.

Configuration:
3-Color Scale:
- Green → Lower case counts
- Yellow → Medium levels
- Red → Higher case counts

Insight:
Visual clustering made infection waves easier to observe.

---

## 4. Sparklines (Trend Visualization)

Purpose:
Display weekly trends of new cases for each country.

Steps:
1. Insert → Line Sparkline
2. Select the weekly data range
3. Enable markers for high and low points

Insight:
Quickly compared trends across countries and years, such as India’s peak in mid-2021.

---

## 5. Data Bars (Visual Indicators)

Purpose:
Provide graphical representation of monthly case totals.

Steps:
1. Select pivot values.
2. Apply Conditional Formatting → Data Bars.
3. Use gradient or solid styles.

Insight:
Wave patterns across months became easier to recognize.

---

## Result
The original COVID dataset was transformed into:
- Weekly and monthly summary tables
- Visual trend indicators
- Tools for identifying clusters and patterns
- Comparative insights across countries and years

---

# Data Preparation using Shell Commands

## 1. File Retrieval
Downloaded a web log dataset from a remote server using the `curl` command.

Result:
A compressed dataset ready for processing.

---

## 2. File Decompression
Used `gzip` to convert the `.gz` archive into a readable log file.

Transformation:
Compressed file → Plain text dataset.

---

## 3. Data Inspection
Used `head` and `tail` commands to preview the first and last lines of the dataset.

Purpose:
Understand the structure of the log entries.

---

## 4. Record Counting
Applied the `wc -l` command to count the total number of entries.

Insight:
Total number of requests recorded during the month.

---

## 5. Field Extraction
Used the `cut` command to isolate specific columns.

Example:
Extracted IP addresses from the first field.

Transformation:
Multi-column log → Single-column IP dataset.

---

## 6. Sorting and Frequency Analysis
Executed a pipeline of commands:

```
cut → sort → uniq → sort
```

Transformation:
Raw IP list → Frequency-ranked IP addresses.

Insight:
Identified which IP addresses generated the most requests.

---

## 7. Pattern Detection
Used the `grep` command with pattern matching.

Purpose:
Identify bot-related traffic such as Googlebot or Applebot.

---

## 8. Log Format Conversion
Used `sed` to replace brackets with quotation marks.

Transformation:
Original log format → CSV-like structure.

---

# Data Preparation using a Text Editor

## 1. JSON Formatting
Reformatted compressed JSON into an organized hierarchical structure.

Transformation:
Compact JSON → Readable structured JSON.

Purpose:
Simplified navigation and data extraction.

---

## 2. Field Extraction
Used multi-cursor selection to extract fields such as **City** and **Product**.

Transformation:
Full dataset → Lists of individual attributes.

---

## 3. Data Sorting
Applied alphabetical sorting to extracted city names.

Transformation:
Unordered list → Sorted dataset.

Purpose:
Easier identification of duplicates.

---

## 4. Duplicate Removal
Removed repeated lines using the editor’s duplicate removal command.

Transformation:
Repeated entries → Unique value list.

---

## 5. Data Standardization
Corrected inconsistent spellings using multi-cursor editing.

Example:
Different spellings of Bangalore standardized as **Bangalore**.

Purpose:
Maintain consistency in categorical data.

---

# Data Cleaning with OpenRefine

## 1. Dataset Import
Loaded the raw dataset into an OpenRefine project environment.

Transformation:
External dataset → Editable OpenRefine project.

---

## 2. Frequency Analysis
Applied **Text Facet** to display value frequencies within columns.

Purpose:
Identify repeated or inconsistent entries.

---

## 3. Similarity Detection
Used clustering algorithms to detect similar textual entries.

Example:
"XYZ Limited" and "XYZ Ltd" grouped together.

---

## 4. Entity Resolution
Merged clustered entries into a single standardized value.

Transformation:
Multiple variations → One consistent entity record.

---

# Data Profiling using Pandas Profiling

## 1. Dataset Import
Loaded the dataset into a pandas DataFrame.

Transformation:
Raw dataset → Structured DataFrame.

---

## 2. Automated Profiling
Generated a profiling report using the Pandas Profiling library.

Transformation:
Dataset → Detailed analytical report.

---

## 3. Distribution Analysis
Visualized distributions for both categorical and numeric variables.

Examples:
- Country frequency
- Population distribution of cities

---

## 4. Outlier Detection
Detected extreme values in numeric variables.

Examples:
- Chongqing with extremely high population.
- Manila with unusually high population density.

---

## 5. Missing Value Analysis
Identified columns with significant missing values.

Example:
Metropolitan population column contained around 50% missing data.

---

## 6. Correlation Analysis
Generated a correlation matrix to examine relationships between variables.

Purpose:
Identify strongly related variables.

---

# JSON API Data Analysis with Python

## 1. API Data Retrieval
Fetched JSON data from the Homebrew API.

Transformation:
Remote API response → Python data structures.

---

## 2. JSON Formatting
Formatted JSON output for readability.

Purpose:
Understand the structure of returned data.

---

## 3. Dynamic URL Generation
Created individual API URLs based on package names.

Transformation:
Package list → Individual analytics endpoints.

---

## 4. Data Extraction
Parsed nested JSON fields to retrieve installation statistics.

Example:
Install counts for 30, 90, and 365 days.

---

## 5. Data Aggregation
Combined extracted fields into structured dictionaries.

Transformation:
Multiple API responses → Unified dataset.

---

## 6. Data Storage
Saved processed results into a JSON file.

Purpose:
Avoid repeated API calls and enable faster analysis.

---

## 7. Data Sorting
Sorted packages based on installation counts.

Transformation:
Unordered package list → Popularity ranking.

---

# Image Processing with Pillow

## 1. Image Loading
Opened images in Python using the Pillow library.

Transformation:
Image files → Python image objects.

---

## 2. Format Conversion
Converted images between formats.

Example:
JPEG → PNG.

---

## 3. Batch Processing
Used loops to apply operations on multiple images in a directory.

Transformation:
Single-image workflow → Automated batch processing.

---

## 4. Image Resizing
Generated thumbnails with specified dimensions.

Example:
300px and 700px versions for web display.

---

## 5. Image Rotation
Rotated images by specified angles.

Example:
90-degree rotation.

---

## 6. Color Conversion
Converted colored images to grayscale.

Purpose:
Produce black-and-white versions for analysis or design.

---

## 7. Image Filtering
Applied Gaussian blur and other filters.

Purpose:
Alter the visual appearance of images.

---

# Media Processing with FFMPEG

## 1. Format Conversion
Converted multimedia files between formats.

Example:
AVI → MP4.

Purpose:
Ensure compatibility across different platforms.

---

## 2. Quality Adjustment
Adjusted video quality using parameters such as quantizer or CRF.

Purpose:
Balance file size and visual quality.

---

## 3. Bitrate Configuration
Specified audio and video bitrate values.

Example:
Video bitrate set to **1000k**.

Purpose:
Control compression level and playback quality.

---

## 4. Audio Processing
Applied audio filters including:
1. Volume adjustments
2. Channel mapping

Purpose:
Improve or modify sound output.

---

## 5. Video Editing
Applied video filters such as:
1. Cropping
2. Scaling
3. Rotation

Purpose:
Modify video dimensions and orientation.
