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

## Summary
This guide covers basic **pandas** functions for data inspection, sorting, filtering, and aggregation. Use these commands to quickly explore and manipulate datasets efficiently!

