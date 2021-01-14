> [tutorial url](https://www.kaggle.com/alexisbcook/hello-seaborn)

# Tutorial


## 1.Set up the notebook

```python
import pandas as pd
pd.plotting.register_matplotlib_converters()
import matplotlib.pyplot as plt
%matplotlib inline
import seaborn as sns
print("Setup Complete")
```


## 2.Load the data

```python
# Path of the file to read
fifa_filepath = "../input/fifa.csv"

# Read the file into a variable fifa_data
fifa_data = pd.read_csv(fifa_filepath, index_col="Date", parse_dates=True)  
```

- index_col : column to use as row labels
- parse_dates : recognize the row labels as dates


## 3.Examine the data

```python
# Print the first 5 rows of the data
fifa_data.head()
```


## 4.Plot the data

```python
# Set the width and height of the figure
plt.figure(figsize=(16,6))

# Line chart showing how FIFA rankings evolved over time 
sns.lineplot(data=fifa_data)
```
