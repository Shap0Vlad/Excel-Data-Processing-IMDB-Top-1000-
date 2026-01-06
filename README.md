Excel-Data-Processing-IMDB-Top-1000
This project focuses on fundamental data analysis tasks within Excel, specifically centering on Data Profiling and Data Cleaning. The goal was to transform a raw dataset into a structured format ready for analysis, demonstrating professional handling of missing values and data integrity.

Data Source
The original dataset was sourced from Kaggle: IMDB Dataset of Top 1000 Movies and TV Shows.

Project Structure
clean_data/: Contains the final processed workbook (clean.xlsx) and preview images of the results.

raw_data/: Contains the original CSV file and evidence of the cleaning process in Power Query.

1. Data Cleaning Workflow (Power Query)
The raw data was processed using Power Query to fix type inconsistencies and "dirty" strings.

Figure 1: Initial data transformation and type standardization in Power Query Editor.

Key transformations:

Type Standardization: Converted "General" types to specific Integer, Decimal, and String formats for all 8 columns.

String Cleaning: Removed non-numeric suffixes from the Runtime column to enable mathematical operations.

Integrity Fix: Identified 1 missing value in the Released_Year column for the movie "Apollo 13" and manually corrected it to 1995.

2. Data Profiling & Imputation
I used a dedicated Meta_data sheet to calculate descriptive statistics and monitor data quality.

Figure 2: Statistical metrics (Mean, Median, STD) and data quality tracking.

Handling Missing Data:

Analysis: Identified 168 missing values in the Gross column.

Method: Applied Median Imputation ($23.5M) to fill the gaps. This method was chosen to maintain the 1000-row sample size while minimizing the bias from high-revenue blockbuster outliers.

3. Visual Analysis (Outlier Detection)
To analyze the revenue distribution and the impact of imputation, I utilized Box and Whisker plots.

Figure 3: Side-by-side comparison of the Original vs. Imputed Gross revenue distribution.

Key Findings:

The charts reveal a significant right-skewed distribution with blockbuster outliers exceeding $900M.

The comparison confirms that median imputation for 16.8% of the data preserved the original statistical trend and did not distort the overall distribution.

Final Preview
The cleaned dataset is now fully optimized for analytical tasks or visualization in BI tools.
