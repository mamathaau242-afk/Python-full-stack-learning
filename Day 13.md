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

## Pandas - Cleaning Empty Cells

### Empty Cells
Empty cells can potentially give you a wrong result when you analyze data.

### Remove Rows
One way to deal with empty cells is to remove rows that contain empty cells.
This is usually OK, since data sets can be very big, and removing a few rows will not have a big impact on the result.

Example:
Return a new Data Frame with no empty cells
```python
import pandas as pd
df = pd.read_csv('data.csv')
new_df = df.dropna()
print(new_df.to_string())
```
### Replace Empty Values
Another way of dealing with empty cells is to insert a new value instead.
This way you do not have to delete entire rows just because of some empty cells.
The fillna() method allows us to replace empty cells with a value:

Example:
Replace NULL values with the number 130
```python
import pandas as pd
df = pd.read_csv('data.csv')
df.fillna(130, inplace = True)
```
### Data of Wrong Format
Cells with data of wrong format can make it difficult, or even impossible, to analyze data.
To fix it, you have two options: remove the rows, or convert all cells in the columns into the same format.

### Removing Rows
The result from the converting in the example above gave us a NaT value, which can be handled as a NULL value, and we can remove the row by using the dropna() method.

Example:
Remove rows with a NULL value in the "Date" column
```python
df.dropna(subset=['Date'], inplace = True)
```
### Replacing Values
One way to fix wrong values is to replace them with something else.
In our example, it is most likely a typo, and the value should be "45" instead of "450", and we could just insert "45" in row 7:

Example:
Set "Duration" = 45 in row 7
```python
df.loc[7, 'Duration'] = 45
```
### Discovering Duplicates
To discover duplicates, we can use the duplicated() method.
The duplicated() method returns a Boolean values for each row:

Example:
Returns True for every row that is a duplicate, otherwise False
```python
print(df.duplicated())
```
### Removing Duplicates
To remove duplicates, use the drop_duplicates() method.

Example:
Remove all duplicates
```python
df.drop_duplicates(inplace = True)
```
