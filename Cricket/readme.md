
## Data Cleaning Steps

1. **Loading the Data:**
   - Load the dataset using pandas `read_csv()` or an appropriate method.
   - I used the [Web Scraper](https://www.webscraper.io/) extension to scrape the content of the [ESPN Cricinfo](https://www.espncricinfo.com/) site for [Records for Test Matches](https://www.espncricinfo.com/records/highest-career-batting-average-282910) 
2. **Changing Column Names:**
   - Rename columns to be more descriptive and consistent.

3. **Checking for Null Values:**
   - Identify missing values (null values) in the dataset using `isnull()` or `info()`.

4. **Filling Null Values:**
   - Fill or impute missing values using methods like `fillna()`.

5. **Checking Duplicates:**
   - Identify duplicate rows using `duplicated()` and check for duplicate values in specific columns if needed.

6. **Dropping Duplicates:**
   - Remove duplicate rows using `drop_duplicates()` to ensure data uniqueness.

7. **Creating New Columns:**
   - Split existing columns to create new ones using methods like `str.split()`.

8. **Converting Column Types:**
   - Convert column data types using `astype()` or specific conversion functions.

9. **Additional Calculations:**
   - Calculate new metrics based on existing data, such as career length, average batting strike rate, etc.

## Data Analysis

- Generate descriptive statistics about the data.
- Visualize the data using various plots and charts.
- Draw insights and conclusions based on the analysis.

## Summary

This repository provides a step-by-step guide to the process of cleaning and analyzing a cricket player statistics dataset. The included code snippets and explanations illustrate each step involved in preparing the data for further analysis and exploration. By following these steps, users can gain valuable insights into the data and uncover interesting patterns and trends.
