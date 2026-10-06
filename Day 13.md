# Day 13

## Key Learnings

### Viewing the Data
One of the most used method for getting a quick overview of the DataFrame, is the head() method.
The head() method returns the headers and a specified number of rows, starting from the top.

Example:
Get a quick overview by printing the first 10 rows of the DataFrame:
```python
import pandas as pd
df = pd.read_csv('data.csv')
print(df.head(10))
```
### tail()
here is also a tail() method for viewing the last rows of the DataFrame.
The tail() method returns the headers and a specified number of rows, starting from the bottom.

Example:
Print the last 5 rows of the DataFrame:
```python
print(df.tail())
```
### Info About the Data
The DataFrames object has a method called info(), that gives you more information about the data set.

Example:
Print information about the data:
```python
print(df.info())`
```
### Data Cleaning
Data cleaning means fixing bad data in your data set.

Bad data could be:
- Empty cells
- Data in wrong format
- Wrong data
- Duplicates
