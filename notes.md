# Got notes
numpy and pandas

# 1 
data training
For data training we need to know how the fuck to make data or get data

simple way get a csv file
then use pandas library

```
```python
import pandas as pd 

file_path_of_csv = ~/Downloads/505/foldername/file.csv
data_for_model = pd.read_csv(file_path_of_csv)
data_for_model.columns
data_for_model.rows
```

Choosing Features
choosing which columns to use to train data, sometimes we dont need all the columns from the file


```python
```
data_feature = ['Rooms', 'Bathrooms', 'Landsize']
x = data_for_model[data_feature]
```

X.describe()
X.head()

Libaray 
scikit-learn libaray to create data_for_model(sklearn)
