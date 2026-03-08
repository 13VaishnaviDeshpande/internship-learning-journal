# Excel Data Cleaning

## Dataset Overview
- Source: Wikipedia city population dataset  
- Fields included: City Name, Country, Population Estimates, City Classification (Municipality / Capital / Autonomous), Area, and other attributes  
- The dataset contains both textual and numeric values  

---

## 1. Using Find and Replace (Ctrl + H)

**Goal:** Remove unwanted text such as “more” appearing inside square brackets in the Country column.

### Procedure
1. Highlight the dataset or the specific column that needs cleaning.  
2. Press `Ctrl + H` to open the **Find and Replace** window.  
3. In the **Find what** field, type the unwanted value (example: `[more]`).  
4. Leave the **Replace with** field empty.  
5. Click **Replace All**.  
6. Check the confirmation message to verify how many replacements were made.  

---

## 2. Converting Data Format (General → Number)

**Goal:** Ensure numeric columns (E–N) are correctly stored as numbers.

### Procedure
1. Select columns **E to N**.  
2. Go to the **Home** tab.  
3. Change the format from **General** to **Number**.  
4. Adjust decimal settings if required.  

---

## 3. Removing Extra Spaces with TRIM()

**Goal:** Eliminate unnecessary spaces from text values.

### Procedure
1. Insert a new column next to the original text column.  
2. Enter the following formula:

```
=TRIM(D2)
```

3. Drag the formula downward to apply it to all rows.  
4. Replace the original column with the cleaned values if needed.  

---

## 4. Locating and Deleting Blank Rows

**Goal:** Remove rows where important fields contain empty values.

### Procedure
1. Select the relevant column (for example, Column D).  
2. Navigate to **Home → Find & Select → Go To Special**.  
3. Choose the **Blanks** option.  
4. Right-click on any highlighted blank cell.  
5. Select **Delete → Entire Row**.  

---

## 5. Removing Duplicate Records

**Goal:** Retain only unique entries in the Country column.

### Procedure
1. Copy the **Country** column to a separate sheet.  
2. Select the column.  
3. Go to **Data → Remove Duplicates**.  
4. Confirm the column selection.  
5. Excel displays the number of removed duplicates and the count of unique values remaining.  

---

# Data Transformation in Excel

## Step 1: Calculating Ratios
- Compute **Metro Area / City Area**.  
- Compute **Metro Population / City Population**.  
- Use **AutoFill** to apply formulas across rows.  
- Carefully handle rows with missing values.  

---

## Step 2: Creating a Pivot Table
- Insert a **Pivot Table** using the entire dataset.  
- Place the pivot table in a new worksheet for analysis.  

---

## Step 3: Detecting Duplicate Country Entries
- Drag **Country** into the **Rows** area.  
- Add **Country** again into the **Values** section and set it to **Count**.  
- This shows how many records exist for each country.  

---

## Step 4: Aggregating Numeric Fields
- Add **City Proper Population** into **Values** and set it to **Sum**.  
- This calculates the total city population per country.  

---

## Step 5: Identifying Outliers
- Insert a **Pivot Chart** (Bar Chart).  
- Apply filters by country.  
- Observe unusual values in:
  - Population  
  - Density ratios  

---

# Splitting Text into Columns in Excel

## Dataset Description
- Source: U.S. Senate voting records copied from a website  
- The entire record was pasted into a single column  
- Data included:
  - Senator Name  
  - Political Party  
  - State  
  - Vote Result (Yea / Nay / Not Voting)  

---

## Problem
All fields were stored in one column separated by different delimiters:

- Left parenthesis `(`  
- Hyphen `-`  
- Right parenthesis `)`  
- Comma `,`  

This format made the dataset unsuitable for analysis.

---

## Step 1: Split by Left Parenthesis `(`
1. Select the column containing the combined text.  
2. Go to **Data → Text to Columns**.  
3. Choose **Delimited**.  
4. Select **Other** and type `(`.  
5. Click **Next → Finish**.  

**Outcome:**  
Senator names are separated from the remaining text.

---

## Step 2: Split by Hyphen `-`
1. Select the newly generated column.  
2. Go to **Data → Text to Columns**.  
3. Choose **Delimited → Other → -**.  
4. Click **Finish**.  

**Outcome:**  
The **Party** field is separated.

---

## Step 3: Split by Right Parenthesis `)`
1. Select the remaining column.  
2. Go to **Data → Text to Columns**.  
3. Choose **Delimited → Other → )**.  
4. Finish the process.  

**Outcome:**  
The **State** field is extracted.

---

## Step 4: Split by Comma `,`
1. Select the final column.  
2. Open **Text to Columns** again.  
3. Choose **Delimited → Comma**.  
4. Finish the operation.  

**Outcome:**  
The **Vote** column (Yea/Nay/Not Voting) is separated.

---

## Step 5: Final Adjustments
- Delete unnecessary intermediate columns.  
- Add headers:
  - Senator  
  - Party  
  - State  
  - Vote  
- Apply proper formatting for readability.  

---

# Data Aggregation in Excel

## Dataset Description
- COVID-19 dataset  
- Fields included:
  - Date  
  - Location (Country)  
  - New Cases  
  - Total Cases  
  - New Deaths  
  - Total Deaths  

---

## Step 1: Remove Irrelevant Columns
- Dropped columns with large numbers of missing values.  
- Retained only:
  - Date  
  - Location  
  - New Cases  

---

## Step 2: Remove Blank Rows
1. Select the **New Cases** column.  
2. Go to **Home → Find & Select → Go To Special**.  
3. Choose **Blanks**.  
4. Right-click and select **Delete → Entire Row**.  

**Outcome:**  
Rows with missing case counts are removed.

---

## Step 3: Convert Dataset into an Excel Table
1. Select the entire dataset.  
2. Click **Insert → Table**.  
3. Enable **My table has headers**.  

**Advantages**
- Built-in filters  
- Automatic formula propagation  
- Structured references  

---

## Step 4: Create Time-Based Columns
Added additional columns:

- Week → `=WEEKNUM(Date,1)`  
- Month → `=TEXT(Date,"mmm")`  
- Year → `=TEXT(Date,"yyyy")`  

Adjusted formatting by converting the **Week** column to a number and removing decimals.

**Outcome:**  
Dataset can now be analyzed by week, month, or year.

---

# Data Preparation Using the Shell

## Dataset Description
- Web server log file from April 2024  
- Fields included:
  - IP Address  
  - Timestamp  
  - Request  
  - HTTP Status Code  
  - Response Size  
  - Referral Source  
  - User Agent  

---

## Step 1: Download the Dataset

Command:

```
curl --location --continue-at - --output s.net-April-2024.log.gz <URL>
```

Purpose:
- Download the dataset from a remote source  
- Follow redirects automatically  
- Save the compressed file locally  

---

## Step 2: Verify File Download

Commands:

```
ls
ls -l
```

Purpose:
- List files in the directory  
- Confirm file size and successful download  

---

## Step 3: Decompress the Log File

Command:

```
gzip --decompress s.net-April-2024.log.gz
```

Purpose:
Convert the compressed log file into a readable text file.

---

## Step 4: Preview File Content

Commands:

```
head -n 5 filename
tail -n 5 filename
```

Purpose:
Inspect the beginning and end of the log file to understand its structure.

---

## Step 5: Count Total Requests

Command:

```
wc -l filename
```

Purpose:
Count the total number of log entries.

---

## Step 6: Extract IP Addresses

Command:

```
cut -d " " -f1 filename
```

Purpose:
Extract the first column containing IP addresses.

---

## Step 7: Identify High-Traffic IPs

Command pipeline:

```
cut -d " " -f1 filename | sort | uniq -c | sort -n
```

Purpose:
- Count requests per IP address  
- Identify the most frequent visitors  

---

## Step 8: Search for Bot Traffic

Command:

```
grep "bot" filename
```

Purpose:
Locate requests made by automated crawlers.

---

## Step 9: Convert Log Format

Used `sed` to modify log structure and create a CSV-like format.

Purpose:
Prepare the file for spreadsheet analysis.

---

## Step 10: Export a Smaller Sample

Command:

```
head -n 1000 log.csv > small.csv
```

Purpose:
Generate a smaller dataset for easier Excel analysis.

---

# Data Preparation in the Editor

## Dataset Description
- JSON dataset containing sales records  
- Fields included:
  - City  
  - Product  
  - Sales  

Initially the JSON file was compressed and difficult to read.

---

## Step 1: Format the JSON File

Steps:
1. Open the file in **Visual Studio Code**.  
2. Press `Ctrl + Shift + P`.  
3. Choose **Format Document**.  

Purpose:
Make the JSON structure readable.

---

## Step 2: Extract City Values

Steps:
1. Search for the word **city** using `Ctrl + F`.  
2. Press `Alt + Enter` to select all matches.  
3. Use `Shift + End` to extend selection.  
4. Copy the values to a new file.  

Outcome:
List of city names extracted.

---

## Step 3: Extract Product Values
Repeat the same process for the **Product** field.

---

## Step 4: Sort Extracted Data

Steps:
1. Open the command palette (`Ctrl + Shift + P`).  
2. Choose **Sort Lines Ascending**.

Purpose:
Arrange values alphabetically.

---

## Step 5: Remove Duplicate Entries

Steps:
1. Open command palette.  
2. Select **Delete Duplicate Lines**.

Outcome:
Unique list of cities obtained.

---

## Step 6: Standardize Inconsistent Values

Example issue:
- "Bangalore" spelled in multiple ways.

Steps:
1. Use `Ctrl + F` to locate variations.  
2. Press `Alt + Enter` to select all occurrences.  
3. Edit them simultaneously using multi-cursor editing.

Outcome:
All city names standardized.

---

## Final Result
Cleaned dataset with:
- Proper formatting  
- Extracted fields  
- Sorted values  
- Duplicate removal  
- Standardized city names  

---

# Data Cleaning with OpenRefine

## Dataset Description
Dataset from the **U.S. Department of Justice** containing:

- Case ID  
- Trade Name  
- Legal Name  
- Street Address  

Multiple records referred to the same entity but had formatting differences.

---

## Step 1: Import Dataset
1. Install and launch **OpenRefine**.  
2. Click **Create Project**.  
3. Upload the dataset.  
4. Click **Next → Create Project**.

Purpose:
Load the dataset into OpenRefine.

---

## Step 2: Detect Inconsistent Entries
Example:

- “XYZ Limited”  
- “XYZ Ltd”

Both refer to the same company but appear as separate values.

---

## Step 3: Create Text Facet

Steps:
1. Click the column dropdown.  
2. Select **Facet → Text Facet**.

Purpose:
View frequency distribution of values.

---

## Step 4: Apply Clustering

Steps:
1. Click **Cluster** in the facet panel.  
2. Review suggested groups of similar entries.

Example cluster:

- "9227 Haven Avenue Suite 330"  
- "9227 Haven Avenue Suite 330.,"

---

## Step 5: Merge Similar Values

Options:
- Merge clusters manually  
- Or use **Merge Selected & Re-cluster**

Purpose:
Standardize entity names and addresses.

---

## Final Result
Dataset with:
- Standardized entity names  
- Merged duplicate addresses  
- Improved data consistency  

---

# Data Profiling with Python

## Dataset Description
Dataset containing information about major cities including:

- Country  
- City population  
- Population density  
- Urban area population  
- Metropolitan population  

Analysis performed using **Pandas Profiling**.

---

## Step 1: Import Libraries

Example:

```
import pandas as pd
from pandas_profiling import ProfileReport
```

Purpose:
Load tools required for automated analysis.

---

## Step 2: Load Dataset

Example:

```
df = pd.read_csv("dataset.csv")
```

Purpose:
Store the dataset inside a pandas DataFrame.

---

## Step 3: Generate Profile Report

Example:

```
profile = ProfileReport(df)
```

Purpose:
Automatically analyze dataset statistics.

---

## Step 4: Export Report

Example:

```
profile.to_file("report.html")
```

Purpose:
Save the profiling results as an HTML report.

---

## Step 5: Review Dataset Insights

The report provides:

- Total variables  
- Number of observations  
- Missing values  
- Distribution of numerical and categorical variables  

---

## Step 6: Detect Outliers

Examine unusual values in fields such as:

- City population  
- Population density  

---

## Step 7: Analyze Correlations

Example relationship:

- Urban area population vs metropolitan population.

Purpose:
Identify highly related variables.

---

## Final Result
Automated report highlighting:
- Data distributions  
- Missing values  
- Correlations  
- Outliers  

---

# JSON API Analysis with Python

## Dataset Description
Homebrew JSON API containing package information and installation analytics.

Fields extracted:

- Package Name  
- Description  
- Install counts (30 / 90 / 365 days)

---

## Step 1: Import Libraries

Example:

```
import requests
import json
import time
```

Purpose:
Enable API requests and JSON processing.

---

## Step 2: Fetch Package List

Example:

```
r = requests.get(API_URL)
packages_json = r.json()
```

Purpose:
Retrieve package data from the API.

---

## Step 3: Inspect JSON Structure

Example:

```
json.dumps(packages_json, indent=2)
```

Purpose:
View formatted JSON structure.

---

## Step 4: Generate Package URLs

Example:

```
package_url = f"{base_url}/{package_name}.json"
```

Purpose:
Access analytics data for individual packages.

---

## Step 5: Extract Installation Data

Fields collected:

- Installs in last 30 days  
- Installs in last 90 days  
- Installs in last 365 days  

---

## Step 6: Loop Through Packages

Use a loop to retrieve analytics for each package automatically.

---

## Step 7: Store Results

Example structure:

```
{
"name": package_name,
"description": description,
"analytics": {
"30d": installs_30,
"90d": installs_90,
"365d": installs_365
}
}
```

---

## Step 8: Save Data to JSON

Example:

```
json.dump(results, file, indent=2)
```

Purpose:
Store collected data locally.

---

## Step 9: Sort Packages by Popularity

Create a sorting function to rank packages based on installation counts.

---

## Final Result
Structured dataset containing package details and installation statistics ranked by popularity.

---

# Image Processing with Pillow (Python)

## Dataset
JPEG image files used for resizing and format conversion.

---

## Step 1: Install Pillow

```
pip install pillow
```

Purpose:
Enable image processing capabilities.

---

## Step 2: Import Modules

```
from PIL import Image
from PIL import ImageFilter
```

---

## Step 3: Open an Image

```
img = Image.open("image.jpg")
```

---

## Step 4: Display Image

```
img.show()
```

---

## Step 5: Convert Image Format

```
img.save("image.png")
```

---

## Step 6: Process Multiple Images

```
for file in os.listdir():
    if file.endswith(".jpg"):
        img = Image.open(file)
```

---

## Step 7: Resize Images

```
img.thumbnail((300,300))
```

---

## Step 8: Save Processed Image

```
img.save("300/image_300.jpg")
```

---

## Step 9: Apply Image Transformations

Examples:

```
img.rotate(90)
img.convert("L")
img.filter(ImageFilter.GaussianBlur)
```

---

## Final Result
Automated script that resizes, converts, and modifies large batches of images.

---

# Media Processing with FFMPEG

## Tool
FFMPEG command-line multimedia processing tool.

---

## Step 1: Install FFMPEG
Download the static build from the official website.

---

## Step 2: Place Executable
Extract the binary and optionally add it to the system **PATH**.

---

## Step 3: Open Command Line
Navigate to the folder containing the media file.

---

## Step 4: Basic Conversion

```
ffmpeg -i input_file output_file
```

Example:

```
ffmpeg -i video.avi video.mp4
```

---

## Step 5: Adjust Output Quality

Examples:

- AVI quality → `-q`  
- MP4 quality → `-crf`

---

## Step 6: Set Bitrates

Example:

```
-b:v 1000k
```

---

## Step 7: Apply Filters

Possible filters include:

- Volume adjustment  
- Audio channel mapping  
- Video cropping  
- Video scaling  
- Video rotation  

---

## Final Result
Media files converted, edited, and optimized using FFMPEG command-line operations.
