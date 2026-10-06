# Day 1

## Key Learnings

###  Pandas
Pandas is a Python library used for working with data sets.
It has functions for analyzing, cleaning, exploring, and manipulating data.
The name "Pandas" has a reference to both "Panel Data", and "Python Data Analysis" and was created by Wes McKinney in 2008.
```python
import pandas as pd
car = {
    "brands": ["Porsche", "Rolls-Royce", "BMW", "Benz", "Ferrari", "Lamborghini"],
    "price": [2000000, 500000, 102000, 1000000, 400000, 500000]
}
cardata=pd.DataFrame(car)
print(cardata)
print(car)
print(cardata[cardata["brands"] == "BMW"])
```
### Checking Pandas Version
The version string is stored under __version__ attribute.

Example:
```python
import pandas as pd
print(pd.__version__)
```
### Pandas Series
Series
A Pandas Series is like a column in a table.
It is a one-dimensional array holding data of any type.
Example:
Create a simple Pandas Series from a list
```python
import pandas as pd
a = [1, 2, 3]
b = pd.Series(a)
print(b)
```
### Create Labels
With the index argument, you can name your own labels.

Example
Create your own labels:
```python
import pandas as pd
a = [1, 2, 3, 4]
b = pd.Series(a, index = ["W","x", "y", "z"])
print(b)
```
### DataFrame
A Pandas DataFrame is a 2 dimensional data structure, like a 2 dimensional array, or a table with rows and columns.
```python
import pandas as pd
a = {"day1": 120, "day2": 280, "day3": 390}
b = pd.Series(a)
print(b)
```
### Locate Row
As you can see from the result above, the DataFrame is like a table with rows and columns.
Pandas use the loc attribute to return one or more specified row(s)
Example:
Return row 0
```python
print(df.loc[0])
```
