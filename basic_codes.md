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

