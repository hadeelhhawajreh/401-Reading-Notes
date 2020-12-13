## The pandas

The pandas package is the most important tool in the field of Data Scientists and Analysts working in Python today.

Pandas is a high-level data manipulation tool developed by Wes McKinney. It is built on the Numpy package meaning a lot of the structure of NumPy is used or replicated in Pandas. Data in pandas is often used to feed statistical analysis in SciPy, plotting functions from Matplotlib, and machine learning algorithms in Scikit-learn.


 dataframe, we have to iterate a dataframe like a dictionary.
...
Iterating over rows and columns.
Function	 Description
index()	   Method returns index (row labels) of the DataFrame
insert()	 Method inserts a column into a DataFrame

The primary two components of pandas are the Series and DataFrame. A Series is essentially a column, and a DataFrame is a multi-dimensional table made up of a collection of Series.
```

In [1]: import numpy as np

In [2]: import pandas as pd
```


Object creation

Creating a Series by passing a list of values, letting pandas create a default integer index:
```
In [3]: s = pd.Series([1, 3, 5, np.nan, 6, 8])

In [4]: s
Out[4]: 
0    1.0
1    3.0
2    5.0
3    NaN
4    6.0
5    8.0
dtype: float64
```

Creating a dataframe using List: DataFrame can be created using a single list or a list of lists.
```
# import pandas as pd
import pandas as pd
 
# list of strings
lst = ['Geeks', 'For', 'Geeks', 'is', 
            'portal', 'for', 'Geeks']
 
# Calling DataFrame constructor on list
df = pd.DataFrame(lst)
print(df)
```
