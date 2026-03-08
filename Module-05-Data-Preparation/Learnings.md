# Data Cleaning in Excel

1. Data cleaning is the initial and essential step before starting any analysis.
2. Excel includes several built-in features that help with quick data preprocessing.
3. The **Find and Replace** tool is useful for eliminating repetitive or unwanted text patterns.
4. Ensuring the correct data type (Text vs Number) is important for performing reliable calculations.
5. The **TRIM()** function removes leading and trailing spaces that may interfere with sorting or filtering.
6. Blank cells can be located and removed using the **Go To Special** option.
7. Removing duplicate entries ensures the dataset contains only unique records.
8. Excel works well for small to medium-sized datasets where manual verification is possible.
9. Proper formatting of data improves both readability and accuracy.
10. Clean and structured data leads to more reliable analysis and visualization results.

---

# Data Transformation in Excel

1. Ratios help reveal meaningful relationships between different variables.
2. Excel formulas make it easy to transform raw numeric values.
3. The **AutoFill** feature speeds up applying formulas across multiple rows.
4. Missing values may lead to calculation errors, so they must be handled carefully.
5. **Pivot Tables** provide a powerful way to summarize and analyze data.
6. Duplicate entries can be identified using count-based aggregation.
7. Pivot Tables support hierarchical grouping such as **Country → City**.
8. Aggregation functions like **Sum** and **Count** quickly generate statistical insights.
9. Pivot charts help visualize summarized data effectively.
10. Bar charts can make outliers easier to detect visually.
11. Excel supports both data transformation and analytical summarization.
12. Transforming cleaned data improves interpretation and analytical value.

---

# Converting Text to Columns in Excel

1. The **Text to Columns** feature is useful when organizing scraped or combined text data.
2. Delimiters allow a single column of text to be split into structured fields.
3. Complex strings may require multiple splitting steps.
4. Excel supports two splitting approaches: **Delimited** and **Fixed Width**.
5. Common delimiters include commas, hyphens, and parentheses.
6. Structuring the data into columns improves readability and usability.
7. Adding clear column headers makes the dataset easier to understand.
8. Well-structured tabular data is necessary before performing analysis.
9. Text to Columns also simplifies conversion of data into CSV format.
10. Excel can serve as a quick preprocessing tool for web-scraped datasets.

---

# Data Aggregation in Excel

1. Data aggregation summarizes large datasets into meaningful insights.
2. Handling missing values is important before performing aggregation.
3. Converting the dataset into an **Excel Table** improves workflow efficiency.
4. Functions such as **WEEKNUM** and **TEXT** help extract time-related attributes.
5. Pivot Tables support multi-level aggregation (for example **Country → Week → Year**).
6. **Value Field Settings** allow operations such as Sum, Average, or Maximum.
7. **Color Scales** help highlight patterns or clusters visually.
8. **Sparklines** provide compact visual representations of trends.
9. **Data Bars** offer quick visual comparisons between values.
10. Aggregated results reveal trends that may not be visible in raw data.
11. Visualization techniques improve insight discovery.
12. Excel can support both data preparation and exploratory analysis tasks.

---

# Data Preparation Using the Shell

1. The Unix shell offers powerful utilities for quick data preparation.
2. Command-line tools are highly efficient because many are written in C.
3. Data pipelines allow multiple commands to be combined into a single workflow.
4. The **curl** command is commonly used to download datasets from URLs.
5. The **ls** command helps confirm file existence and check file size.
6. **gzip** is used to compress or decompress data files.
7. **head** and **tail** allow quick previews of large datasets.
8. **wc -l** counts the number of lines in a file.
9. **cut** extracts specific columns from structured text files.
10. **sort** organizes data for easier processing.
11. **uniq -c** counts unique values in sorted datasets.
12. **grep** performs pattern matching using regular expressions.
13. Command pipelines enable efficient data transformation.
14. **sed** can modify or reformat text streams.
15. Shell tools are commonly used to prepare data before loading it into Excel, Python, or other analysis tools.

---

# Data Preparation in a Text Editor

1. Text editors such as **Visual Studio Code** can assist in quick data preparation tasks.
2. Formatting JSON files improves readability and structure.
3. The **Command Palette (Ctrl + Shift + P)** provides access to powerful editing features.
4. **Multi-cursor editing** allows simultaneous editing of multiple locations in a file.
5. **Alt + Enter** can select all occurrences of a search term.
6. Sorting lines helps organize and analyze extracted data values.
7. Removing duplicate lines helps identify unique entries.
8. Search and replace functions help correct inconsistent values.
9. Editors can perform lightweight data cleaning without specialized software.
10. Keyboard shortcuts greatly improve productivity when processing data.

---

# Cleaning Data with OpenRefine

1. **OpenRefine** is an open-source application designed for data cleaning and transformation.
2. It was initially developed as a Google project.
3. Although it runs locally, the interface is accessed through a web browser.
4. It is especially useful for handling messy or inconsistent datasets.
5. **Text Facets** display frequency distributions for column values.
6. Clustering algorithms identify similar text values with small differences.
7. **Entity resolution** helps merge records representing the same real-world entity.
8. OpenRefine supports both manual and automated merging processes.
9. Standardizing categorical values improves aggregation accuracy.
10. The tool is widely used for data cleaning in data analysis workflows.

---

# Data Profiling with Python

1. **Pandas Profiling** is a library that automates exploratory data analysis.
2. It generates a comprehensive dataset report with minimal code.
3. The report includes structure, statistics, and visual summaries.
4. It highlights missing values across variables.
5. Outliers in numerical columns are automatically detected.
6. The report shows distributions for both categorical and numeric data.
7. Correlation analysis helps identify relationships between variables.
8. Automated reports reduce the need for manual exploratory work.
9. The tool helps detect potential data quality issues early.
10. Pandas Profiling is frequently used before building machine learning models.

------

# Image Manipulation with Pillow

1. Pillow is a Python library designed for performing image processing tasks.
2. Images can be opened in Python as objects and then modified using different functions.
3. The library provides features such as resizing, rotating, and applying filters to images.
4. It also supports converting image formats, for example converting a JPEG image into PNG.
5. Multiple images can be processed automatically through batch operations.
6. Thumbnail images can be created while maintaining the original aspect ratio.
7. Python scripts using Pillow help automate repetitive image editing operations.
8. Visual effects like blur filters can be applied to change the appearance of an image.
9. Color images can be converted into grayscale for analysis or preprocessing.
10. Pillow is commonly used in web applications and data pipelines where image preprocessing is required.

---

# Media Processing with FFMPEG

1. FFMPEG is a widely used command-line utility for handling multimedia files.
2. It can convert between many formats of video, audio, and images.
3. The general command structure follows the pattern: `ffmpeg -i input_file output_file`.
4. Output video quality can be adjusted using parameters such as quantizer or CRF values.
5. Bitrate settings allow control over the compression and final file size.
6. FFMPEG includes a large collection of audio and video filters.
7. These filters enable transformations such as cropping, scaling, rotating, and adjusting audio volume.
8. Command-line execution makes it possible to process large numbers of media files efficiently.
9. The tool is commonly used in media production environments, streaming platforms, and data processing workflows.
10. Understanding different command flags allows more advanced media editing and automation tasks.
