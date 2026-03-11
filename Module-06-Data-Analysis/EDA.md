# Exploratory Data Analysis (EDA): Correlation Analysis with Excel

## Overview
This tutorial demonstrates how to perform **correlation analysis** and basic **visual exploration** using Microsoft Excel on a COVID-19 dataset. Correlation analysis measures the **statistical relationship between two variables** and determines how strongly they are linearly related.

The dataset contains the following variables used in the analysis:
- `new_cases`
- `new_deaths`
- `new_vaccinations`

---

## What is Correlation?

Correlation measures the **degree of linear association between two variables**.

Correlation coefficient values range between:

| Value | Meaning |
|------|--------|
| +1 | Perfect positive correlation |
| 0 | No correlation |
| -1 | Perfect negative correlation |

Example:
- `0.84` → Strong positive correlation  
- `0.23` → Weak positive correlation  

---

## Dataset

The COVID-19 dataset contains daily records including:

| Column | Description |
|------|-------------|
| new_cases | Number of new COVID-19 cases reported |
| new_deaths | Number of new COVID-19 deaths reported |
| new_vaccinations | Number of vaccinations administered |

For this analysis, only these three columns are used.

---

## Step 1: Enable Excel Data Analysis ToolPak

1. Open **Excel**
2. Click **File**
3. Select **Options**
4. Go to **Add-ins**
5. In **Manage**, select **Excel Add-ins**
6. Click **Go**
7. Check **Analysis ToolPak**
8. Click **OK**

After enabling, the **Data Analysis** option appears in the **Data tab**.

---

## Step 2: Prepare the Dataset

Keep only the required columns:

new_cases  
new_deaths  
new_vaccinations  

Remove other columns to simplify the analysis.

---

## Step 3: Generate Correlation Matrix

Steps:

1. Go to **Data**
2. Click **Data Analysis**
3. Select **Correlation**
4. Click **OK**
5. Select the input range containing:

new_cases  
new_deaths  
new_vaccinations  

6. Check **Labels in First Row**
7. Select an **Output Range**
8. Click **OK**

---

## Correlation Matrix Example

| Variable | new_cases | new_deaths | new_vaccinations |
|---------|-----------|------------|------------------|
| new_cases | 1 | 0.84 | 0.31 |
| new_deaths | 0.84 | 1 | 0.23 |
| new_vaccinations | 0.31 | 0.23 | 1 |

---

## Interpretation

### New Cases vs New Deaths
- Correlation = **0.84**
- Indicates **strong positive correlation**
- When cases increase, deaths tend to increase.

### New Vaccinations vs New Deaths
- Correlation = **0.23**
- Indicates **weak positive correlation**
- Relationship exists but is not strong.

---

## Step 4: Visualize Using Scatter Plot

Scatter plots help visualize relationships between variables.

### Plot 1: New Cases vs New Deaths

Steps:

1. Select `new_cases` and `new_deaths`
2. Go to **Insert**
3. Select **Recommended Charts**
4. Choose **Scatter Plot**

Add a **Trendline**:

- Click **Chart Elements (+)**
- Select **Trendline**
- Format line:
  - Color: Red
  - Style: Solid dash
  - Increase thickness

Interpretation:

The upward slope shows **strong positive correlation**.

---

### Plot 2: New Vaccinations vs New Deaths

Steps:

1. Select `new_vaccinations` and `new_deaths`
2. Insert **Scatter Plot**
3. Add **Trendline**

Interpretation:

- Trendline slope is **less steep**
- Indicates **weaker correlation**

Observation:
- Early period: Low vaccinations, high deaths  
- Later period: Increased vaccinations correspond with reduced deaths  

---

## Key Insights

- **New Cases ↔ New Deaths**
  - Strong positive relationship
  - Increased cases are associated with increased deaths

- **New Vaccinations ↔ New Deaths**
  - Weak correlation
  - Vaccinations may contribute to lowering deaths but require deeper analysis

---

## Limitations

Correlation **does not imply causation**.

From this analysis alone, we **cannot conclude** that vaccinations directly reduced deaths. Further analysis such as:

- Regression analysis  
- Time-series analysis  
- Causal modeling  

is required.

---

## Tools Used

- Microsoft Excel  
- Excel Data Analysis ToolPak  
- Scatter Plot Visualization  

---

