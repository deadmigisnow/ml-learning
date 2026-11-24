# One
**Define Target, feature and decision tree**
```txt
**target:** Target is an Outcome of a model, which is trained to predict, it is also caleed a label.


**Feature:** Feature is an measurable property such a cloumns in a csv file, but we only select few or needed features from the file instead of every feature, which is also an input for model to help make predictions.

**Decision Tree:** DecisionTree is an supervised lerning algorithm that is in a tree like structure, the root has branches, with their own possible outcomes for each different branch, its helps to make decisions like YES or NO. 
```


```python
'''self.code
import seaborn as sns
import pandas as pd

# Loading data using seaborn
diamonds = sns.load_dataset("daimonds)
print(diamonds.head())

# Below Chunk to find rows and coulmns of a data/file
df = pd.DataFrame(daimonds)
rows, columns = df.shape
print(f"Rows:{rows}. Columns:{columns}")

# Summary statistics
stat = df.describe()
print(stat)

# Missing Values
miss_val = df.isnull().sum()
print(miss_val)

print(f"Minimum Price: ${diamonds['price'].min()}")
print(f"Maximum Price: ${diamonds['price'].max()}")
print(f"Average: ${diamonds['carat'].mean()}")
'''

import seaborn as sns

diamonds = sns.load_dataset("diamonds")
print(diamonds.head())

rows, columns = diamonds.shape
print(f"Rows: {rows}, Columns: {columns}")

print(diamonds.describe())
print(diamonds.isnull().sum())

print(f"Price range: ${diamonds['price'].min()} to ${diamonds['price'].max()}")
print(f"Average carat: {diamonds['carat'].mean():.2f}")

```

|Functions|Descriptions|
|---|---|
|.isnull()|Detect missing values|
|.notnull()|Detect non-missing values|
|.info()|Summary with missing counts|
|.isna()|Same as isnull().|
|dropna()|Remove missing rows/columns|
|fillna()|Fill missing values|
|replace()|Replace specific values|
|drop_duplicates()|Remove duplicate rows|
|unique()|Get unique values in a Series/DataFrame|

## Difference in DataFrame and Series
**DataFrame:** Two-Dimensional, tabular data Structure with rows and columns, 
Dataframe has three main components: the data, which are stored in rows and columns., rows are labeled as index and columns are labeled and contains the actual data.

**Series:** One-dimensional array object that can hold data of any type such as int,float,string,etc.
labeled each element has a unique identity called index.

# X.head()
The `.head()` method is a built-in pandas function that returns the first five rows of a dataframe or series by default. It is used to quickly inspect the structure and initial values of data without printing the entire, potentially massive, dataset to the console.