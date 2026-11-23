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
```
X.describe()
X.head()

Libaray 
scikit-learn libaray to create data_for_model(sklearn)
This md is mainly about learning about deicision tree model type
define: ask question to yourself what type of this model will be i know the answer deicision tree Dwww
Fit: Capturing patterns from provide data
predict:predict 
And evaluate how accurate the mode predict

```python
from skllearn.tree import DecisionTreeRegressor

data_model = DecisionTreeRegressor(random_state=1)
data_model.fit(X,y)

## Model Validation 
Measuring the performance of the model
Mean ABsolute Error also called as MAE
to calulcate the mean absolute Error
using sklearn.metrics import mean_absolute_error
this is called In-sample scores
Validation data topic????
scikit-learn has a function called train_test_spilt to break up the data into two pieces.
sklearn.model_selection import train_test_spilt

# Overfitting and UnderFitting

Overfitting: Capturing spurious patterns that wont recurw in the future, leading to less accurate predictions
Underfitting: failing  to capture relevant patterns, again leading to less accurate predictions.

# Random Forests
basic idea builds many Decision trees during training and output the average prediction or the majority vote from all the trees.
from sklearn.ensemble import RandomForestsRegressor
```python
forest_model = RandomForestsRegressor(random_state=1)

```
