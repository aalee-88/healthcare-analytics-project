# Healthcare Patient Analytics
A data analytics portfolio project analyzing 55,000+ patient records to identify trends in hospital admissions, billing costs, and patient demographics.

## Tools & Technologies
- **PostgreSQL** — data storage, cleaning, and analysis via SQL queries
- **Power BI** — interactive dashboard with charts and slicers
- **Excel** — initial data preview
- **Kaggle** — data source

## Project Structure
```
Healthcare_BA_Project/
├── Results_SQL_Questions/       # .txt files with query results
├── Healthcare Analytics Project Documentation.pdf  # Full project walkthrough, includes all SQL queries
├── Healthcare_Dashboard.pbix    # Power BI dashboard file
├── Healthcare_Dashboard.pdf     # Dashboard screenshot export
└── healthcare_dataset.csv       # Source data
```

## What the Project Covers

**Data Cleaning (SQL)**
- Checked for NULLs and duplicates
- Removed ~5,500 duplicate rows using `ctid`
- Standardized patient name formatting with `INITCAP()`

**Data Analysis (SQL)**
- Most common medical conditions
- Average billing by condition and insurance provider
- Admission type breakdown using `OVER()` window functions
- Average hospital stay length via date arithmetic
- Patient demographics by age group using `CASE WHEN`
- Test result distribution

**Dashboard (Power BI)**
- 6 chart types: clustered bar, column, donut, treemap, pie, and slicer
- DAX calculated column for age groups using `SWITCH()`
- DAX measure for average stay days using `AVERAGEX()` and `DATEDIFF()`

## Key Insights
- Billing is nearly uniform across all conditions (~$25,234–$25,784), suggesting standardized pricing in the dataset — in real-world data, conditions like Cancer would typically incur significantly higher costs.
- Obesity generates the highest average billing despite ranking 5th in patient volume, indicating a disproportionate cost burden relative to its prevalence.
- Admission types and test results each split almost perfectly into thirds, a distribution pattern uncommon in real hospital data and consistent with synthetic     dataset generation.

## Data Source
[Healthcare Dataset by Prasad Patil](https://www.kaggle.com/datasets/prasad22/healthcare-dataset) — Kaggle
