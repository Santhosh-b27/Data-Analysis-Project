  # Zomato Stock Price Analysis

This project analyzes the stock prices of Zomato using Python libraries like Pandas, Seaborn, and Matplotlib. The analysis includes descriptive statistics, visualizations, and insights into the stock's opening, high, and low prices.

## Project Structure

- `data/`: Contains the dataset `Zomato_Dataset.csv`.
- `notebooks/`: Contains the Jupyter notebook `Zomato_Stock_Analysis.ipynb` with the analysis code.
- `README.md`: Provides an overview of the project.

## Setup Instructions


1.Clone the repository:
   
   ```bash
   git clone https://github.com/your-username/Zomato_Stock_Analysis.git
   cd Zomato_Stock_Analysis
   ```
   
2.Install the required packages:

   ```bash
   
   pip install pandas numpy matplotlib seaborn
```

3.Run the Jupyter notebook:

   ```bash
   jupyter notebook notebooks/Zomato_Stock_Analysis.ipynb

```
# Analysis Overview
## Import Libraries

The analysis starts by importing necessary libraries for data manipulation and visualization.

```python

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
## Load Dataset
 Load the dataset from the data directory.

```python

df = pd.read_csv("../data/Zomato_Dataset.csv")
```
Initial Data Exploration
Display the first and last few rows of the dataset to understand its structure.

## First 5 Row Need Means
```python

print("First 5 rows of the dataset:")
display(df.head())
```
## Last 5 Row need means
```python
print("Last 5 rows of the dataset:")
display(df.tail())
```
# Display dataset information to get details about the data types and missing values.

```python

print("Dataset information:")
df.info()
Display descriptive statistics to understand the distribution of the data.
```
## Describe the Dataset
```python
print("Descriptive statistics:")
display(df.describe())
Transpose the descriptive statistics for better readability.
```
## Describe the dataset into Transpose
```python

print("Transposed descriptive statistics:")
display(df.describe().T)
Display descriptive statistics for object-type columns to get an overview of categorical data.
```
## Descriptive Statistics
```python

print("Descriptive statistics for object type columns:")
display(df.describe(include='object'))
Min and Max Prices
Calculate and print the minimum and maximum opening prices.
```
## Analysis of MAX & MIN of Stock Value
```python

print(f"Min price is: {df['Open'].min()}$")
print(f"Max price is: {df['Open'].max()}$")
```
# Visualizations
## Generate visualizations to gain insights into the data distribution.

# Histogram for Opening Price
## Plot a histogram for the opening price to visualize its distribution.

```python
plt.figure(figsize=(10, 5))
sns.histplot(df['Open'].dropna(), kde=True, bins=20, color='skyblue')
plt.title('Stock Opening Price')
plt.xlabel('Opening')
plt.ylabel('Frequency')
plt.show()

```
# Histogram for High Price
## Plot a histogram for the high price.

```python

plt.figure(figsize=(10, 5))
sns.histplot(df['High'].dropna(), kde=True, bins=20, color='lightgreen')
plt.title('Stock High Price')
plt.xlabel('High')
plt.ylabel('Frequency')
plt.show()
```
# Histogram for Low Price
## Plot a histogram for the low price.

```python

plt.figure(figsize=(10, 5))
sns.histplot(df['Low'].dropna(), kde=True, bins=20, color='red')
plt.title('Stock Low Price')
plt.xlabel('Low')
plt.ylabel('Frequency')
plt.show()
```
# Boxplot for Opening Price
## Generate a boxplot for the opening stock price to visualize its distribution and identify outliers.

```python


plt.figure(figsize=(10, 6))
sns.boxplot(x='Open', data=df, color='yellow')
plt.title('Open Stock')
plt.xlabel('Open Stock')
plt.ylabel('Price')
plt.show()
```
## Conclusion
This project provides an in-depth analysis of Zomato's stock prices. By following the steps outlined above, you can reproduce the analysis and gain insights into the stock's performance. The visualizations help in understanding the distribution and relationships between different stock prices.
