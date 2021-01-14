> [tutorial url](https://www.kaggle.com/alexisbcook/line-charts)

# Tutorial

## 1. Load the data

```python
# Path of the file to read
spotify_filepath = "../input/spotify.csv"

# Read the file into a variable spotify_data
spotify_data = pd.read_csv(spotify_filepath, index_col="Date", parse_dates=True)
```

## 2. Examine the data

```python
# Print the first 5 rows of the data
spotify_data.head()

# Print the last five rows of the data
spotify_data.tail()
```

## 3. Plot the data

```python
# Line chart showing daily global streams of each song 
sns.lineplot(data=spotify_data)
```
output
![image](https://user-images.githubusercontent.com/74973306/104545174-c9618400-566c-11eb-84ad-4066a4a55085.png)


```python
# Set the width and height of the figure
plt.figure(figsize=(14,6))

# Add title
plt.title("Daily Global Streams of Popular Songs in 2017-2018")

# Line chart showing daily global streams of each song 
sns.lineplot(data=spotify_data)
```
output
![image](https://user-images.githubusercontent.com/74973306/104545225-e39b6200-566c-11eb-86c9-982e09c514aa.png)


### Plot a subset of the data
```python
list(spotify_data.columns)
```
 
```python
# Set the width and height of the figure
plt.figure(figsize=(14,6))

# Add title
plt.title("Daily Global Streams of Popular Songs in 2017-2018")

# Line chart showing daily global streams of 'Shape of You'
sns.lineplot(data=spotify_data['Shape of You'], label="Shape of You")

# Line chart showing daily global streams of 'Despacito'
sns.lineplot(data=spotify_data['Despacito'], label="Despacito")

# Add label for horizontal axis
plt.xlabel("Date")

```

output
![image](https://user-images.githubusercontent.com/74973306/104545342-2c531b00-566d-11eb-9d00-0b09c0df62d4.png)
