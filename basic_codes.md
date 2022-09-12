## Take input from user by a prompt
```python
name = input("What is your name: ")
print(name)
```
### Writing Clear Prompts
Sometimes you’ll want to write a prompt that’s longer than one line. For example, you might want to tell the user why you’re asking for certain input. You can assign your prompt to a variable and pass that variable to the `input()` function. This allows you to build your prompt over several lines, then write a clean `input()` statement. For example:

```python
msg = "I will print your name on the screen"
msg += "\nWhat is your name: "

name = input(msg)
print(name)
```

## Load a csv file
There are several functions for loading csv file in python. Here, I will use most commonly use pandas function

```python
import pandas as pd
df = pd.read_csv("path/to/your/file.csv")
```
### View first 5 line of the dataframe
```python
df.head(5)
```

## Create dictionary from list
Let's say we have following two lists. Then we can use the following codes to create dictionary from these lists.

```python
# Create the years and durations lists
years = list(range(2011,2021))
durations = [103, 101, 99, 100, 100, 95, 95, 96, 93, 90]

# Create a dictionary with the two lists
movie_dict = {"years": years, "durations" : durations}

# Print the dictionary
movie_dict
```

## Creating dataframe from a dictionary
Let's say we have a dictionary which contains lists for each key. In this case, use can use `DataFrame` functions from **pandas** package to create a dataframe.

```python
# Import pandas under its usual alias
import pandas as pd

# Create a DataFrame from the dictionary
durations_df = pd.DataFrame(movie_dict)

# Print the DataFrame
durations_df
```

## Subset a dataframe to keep only specific columns
There are multiple ways to subset a DataFrame for specific columns. If we wanted to subset the music_df DataFrame described above for only album_title, artist, and album_length, we could pass in a list of the columns we want inside the square brackets, as shown below:

```python
music_df[['album_title', 'artist', 'album_length']]
```
## Subset a dataframe based on specific value in a specific column
There are many ways to subset a DataFrame. One way that you have been taught is to use **square brackets**, passing in a condition. For example, if we wanted to subset a `music_df` DataFrame for rows where the column `genre` was `"metal"`, we could use the following:

```python
music_df[music_df["genre"] == "metal"]
```
## Subset a dataframe based on certain condition (less than, grater than etc) in a specific column
We can specify a condition using square brackets in much the same way as we subset the DataFrame for music earlier. Here is another such example on the music_df DataFrame, filtering for album lengths greater than 120 minutes.

```python
music_df[music_df['album_length'] > 120]
```

