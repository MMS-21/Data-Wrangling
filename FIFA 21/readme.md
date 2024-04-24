# Data Cleaning and Visualization Process for FIFA 21 Dataset

## Introduction
This document outlines the steps taken to clean and visualize the FIFA 21 dataset. The dataset contains information about player values, among other attributes.

## 1. Data Cleaning

### 1.1 Loading the Dataset
- Imported the necessary libraries: `pandas` for data manipulation and `matplotlib.pyplot` for visualization.
- Loaded the FIFA 21 dataset into a pandas DataFrame.

```python
import pandas as pd

# Load the dataset
df = pd.read_csv('fifa21_dataset.csv')
```
### 1.2 Cleaning the 'Value' Column
- Created a function clean_value to process the 'Value' column.
- Removed the Euro sign ('€') from the values.
- Converted 'M' values (million) to numeric.
- Converted 'K' values (thousands) to numeric and then to millions.
  
```python
def clean_value(value):
    if 'M' in value:
        return float(value.replace('€', '').replace('M', ''))
    elif 'K' in value:
        return float(value.replace('€', '').replace('K', '')) / 1000
    else:
        return float(value.replace('€', ''))

df['Value'] = df['Value'].apply(clean_value)
```
### 1.3 Data Type Consistency
- Ensured consistency in data types for the 'Value' column.
``` python
df['Value'] = pd.to_numeric(df['Value'])
```
## 2. Visualization
### 2.1 Histogram of Player Values
- Utilized Matplotlib to create a histogram of player values in millions.
``` python
import matplotlib.pyplot as plt

plt.figure(figsize=(10, 6))
plt.hist(df['Value'], bins=10, color='skyblue', edgecolor='black')
plt.title('Distribution of Player Values')
plt.xlabel('Value (in Millions)')
plt.ylabel('Frequency')
plt.grid(True)
plt.show()
```
## Conclusion
- The dataset has been successfully cleaned, and a histogram visualization has been created to analyze the distribution of player values.
