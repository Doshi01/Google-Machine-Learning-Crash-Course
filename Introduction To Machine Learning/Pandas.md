```python
import numpy as np
import pandas as pd
# This Colab introduces DataFrames, which are the central data structure in the pandas API.

# Create and populate a 5x2 NumPy array.
my_data = np.array([[0, 3], [10, 7], [20, 9], [30, 14], [40, 15]])

# Create a Python list that holds the names of the two columns.
my_column_names = ['temperature', 'activity']

# Create a DataFrame.
my_dataframe = pd.DataFrame(data=my_data, columns=my_column_names)

# Print the entire DataFrame
print(my_dataframe)

# Create a new column named adjusted.
my_dataframe["adjusted"] = my_dataframe["activity"] + 2

# Print the entire DataFrame
print(my_dataframe)

my_column_names = ['Eleanor', 'Chidi', 'Tahani', 'Jason']
my_data = np.random.randint(low=0, high=101, size=(3, 4))
df = pd.DataFrame(data=my_data, columns=my_column_names)
print(df)
print("\nSecond row of the Eleanor column: %d\n" % df['Eleanor'][1])
df['Janet'] = df['Tahani'] + df['Jason']

```

Pandas provides two different ways to duplicate a DataFrame:

- Referencing. 
If you assign a DataFrame to a new variable, any change to the DataFrame or to the new variable will be reflected in the other.
- Copying. 
If you call the pd.DataFrame.copy method, you create a true independent copy. Changes to the original DataFrame or to the copy will not be reflected in the other.

```python

# Create a reference by assigning my_dataframe to a new variable.
print("Experiment with a reference:")
reference_to_df = df

# Print the starting value of a particular cell.
print("  Starting value of df: %d" % df['Jason'][1])
print("  Starting value of reference_to_df: %d\n" % reference_to_df['Jason'][1])

# Modify a cell in df.
df.at[1, 'Jason'] = df['Jason'][1] + 5
print("  Updated df: %d" % df['Jason'][1])
print("  Updated reference_to_df: %d\n\n" % reference_to_df['Jason'][1])

# Create a true copy of my_dataframe
print("Experiment with a true copy:")
copy_of_my_dataframe = my_dataframe.copy()

# Print the starting value of a particular cell.
print("  Starting value of my_dataframe: %d" % my_dataframe['activity'][1])
print("  Starting value of copy_of_my_dataframe: %d\n" % copy_of_my_dataframe['activity'][1])

# Modify a cell in df.
my_dataframe.at[1, 'activity'] = my_dataframe['activity'][1] + 3
print("  Updated my_dataframe: %d" % my_dataframe['activity'][1])
print("  copy_of_my_dataframe does not get updated: %d" % copy_of_my_dataframe['activity'][1])
```