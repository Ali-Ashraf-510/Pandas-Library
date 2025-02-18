# Pandas Basics - Quick Reference Guide
![image](https://github.com/user-attachments/assets/17dd7938-17b6-41d1-9dc4-7f104acc4c9d)


## 1. Inspecting Data

```python
# Display dataset structure, data types, and missing values
df.info()
```

```python
# Show statistics for numerical columns
df.describe()
```

## 2. Sorting Data

```python
# Sort data ascending by the specified column
df.sort_values(by='column_name')
```

```python
# Sort data descending
df.sort_values(by='column_name', ascending=False)
```

```python
# Sort by multiple columns (first ascending, second descending)
df.sort_values(by=['col1', 'col2'], ascending=[True, False])
```

```python
# Sort and modify the DataFrame in place
df.sort_values(by='column_name', inplace=True)
```

## 3. Unique & Value Counts

```python
# Get unique values in a column
df['column_name'].unique()
```

```python
# Count occurrences of each unique value
df['column_name'].value_counts()
```

## 4. Filtering Data

```python
# Filter rows where a column equals a specific value
df[df['column_name'] == 'value']
```

```python
# Filter using OR condition
df[(df['col1'] == 'value1') | (df['col2'] < value2)]
```

```python
# Filter using AND condition
df[(df['col1'] == 'value1') & (df['col2'] < value2)]
```

## 5. Grouping & Aggregation

```python
# Group data and calculate the mean
df.groupby('column_name')['target_column'].mean()
```

```python
# Apply multiple aggregation functions
df.groupby('column_name')['target_column'].agg(['mean', 'min', 'max'])
```

```python
# Group by multiple columns and find min/max values
df.groupby(['col1', 'col2'])['target_column'].agg(['min', 'max'])
```

## 6. Handling Missing Data

```python
# Check for missing values in each column
df.isnull().sum()

# Drop rows with any missing values
df.dropna()

# Drop columns with any missing values
df.dropna(axis=1)

# Fill missing values with a specific value
df.fillna(value)

# Fill missing values with the mean of the column
df['column_name'].fillna(df['column_name'].mean(), inplace=True)
```

## 7. Adding and Removing Columns

```python
# Add a new column
df['new_column'] = df['existing_column'] * 2

# Remove a column
df.drop('column_name', axis=1, inplace=True)

# Rename columns
df.rename(columns={'old_name': 'new_name'}, inplace=True)
```

## 8. Saving and Loading Data

```python
# Save DataFrame to a CSV file
df.to_csv('filename.csv', index=False)

# Load data from a CSV file
df = pd.read_csv('filename.csv')

# Save DataFrame to an Excel file
df.to_excel('filename.xlsx', index=False)

# Load data from an Excel file
df = pd.read_excel('filename.xlsx')
```

## 9. Indexing and Selecting Data

```python
# Select a single column
df['column_name']

# Select multiple columns
df[['col1', 'col2']]

# Select rows by index
df.iloc[0:5]  # First 5 rows

# Select rows by label
df.loc[df['column_name'] == 'value']

# Set a column as the index
df.set_index('column_name', inplace=True)

# Reset the index
df.reset_index(inplace=True)
```
## 10. Handling Duplicates

```python
# Check for duplicate rows
df.duplicated().sum()

# Drop duplicate rows
df.drop_duplicates(inplace=True)

# Drop duplicates based on specific columns
df.drop_duplicates(subset=['col1', 'col2'], inplace=True)
```
## Summary
This guide covers basic **pandas** functions for data inspection, sorting, filtering, and aggregation. Use these commands to quickly explore and manipulate datasets efficiently!


