# `1.1.6: The AI Data Wrangler: Intro to Pandas`

**Context & Relevance:** Now that you're comfortable with NumPy for numerical operations, it's time to meet Pandas - the workhorse library for data manipulation in Python. While NumPy is great for homogeneous numerical data, real-world data is messy, heterogeneous, and comes with labels. Pandas provides the perfect tools for cleaning, transforming, and analyzing this type of data, making it absolutely essential for AI and data science work.

## 1. Introduction & Overview

Think of Pandas as Excel on steroids for Python. It provides powerful, flexible, and efficient data structures for working with structured (tabular, multidimensional, potentially heterogeneous) data. Most AI projects spend about 80% of their time on data preparation, and Pandas is the primary tool for this crucial task.

In this lesson, you'll learn about the two fundamental Pandas data structures - Series and DataFrames - and how to perform basic data manipulation tasks that form the foundation of AI data preprocessing.

## 2. Basic Concepts & Definitions

*   **Pandas:** A Python library providing high-performance, easy-to-use data structures and data analysis tools.
    *   *Analogy:* If NumPy is a calculator for numbers, Pandas is a Swiss Army knife for data tables.
*   **DataFrame:** A 2-dimensional labeled data structure with columns of potentially different types, similar to a spreadsheet or SQL table.
*   **Series:** A 1-dimensional labeled array capable of holding any data type, similar to a single column in a spreadsheet.
*   **Index:** The row labels of a DataFrame or Series.
*   **NaN:** "Not a Number" - Pandas' representation of missing data.

## 3. Detailed Explanations

### Why Pandas is Essential for AI

Pandas solves critical data handling challenges:
1. **Handles missing data** - Provides tools to detect, remove, or fill missing values
2. **Size mutability** - Columns can be inserted and deleted from DataFrames
3. **Automatic alignment** - Operations automatically align on index labels
4. **Powerful grouping** - Group data for aggregations and transformations
5. **Time series functionality** - Specialized tools for working with time-based data

### Core Pandas Data Structures

```python
import pandas as pd  # Standard import convention
import numpy as np

# Creating a Series (1D)
data = pd.Series([0.25, 0.5, 0.75, 1.0])
print("Series:")
print(data)
print("Values:", data.values)
print("Index:", data.index)

# Creating a DataFrame (2D)
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Diana'],
    'Age': [25, 30, 35, 28],
    'City': ['New York', 'London', 'Paris', 'Tokyo']
}
df = pd.DataFrame(data)
print("\nDataFrame:")
print(df)
```

## 4. Practical Examples & Code Samples

Let's explore practical Pandas operations for AI data preparation:

```python
import pandas as pd
import numpy as np

# Creating a sample DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Diana', 'Evan'],
    'Age': [25, 30, 35, 28, np.nan],
    'Salary': [50000, 60000, 70000, 55000, 48000],
    'Department': ['Engineering', 'Sales', 'Engineering', 'Marketing', 'Sales']
}
df = pd.DataFrame(data)
print("Original DataFrame:")
print(df)

# Basic DataFrame operations
print("\nDataFrame Info:")
print("Shape:", df.shape)  # (rows, columns)
print("Columns:", df.columns.tolist())
print("First 2 rows:\n", df.head(2))
print("Data types:\n", df.dtypes)

# Selecting data
print("\nSelection Examples:")
print("Ages column:\n", df['Age'])
print("Multiple columns:\n", df[['Name', 'Salary']])
print("First row:\n", df.iloc[0])  # By position
print("Row with index 2:\n", df.loc[2])  # By label

# Filtering data
print("\nFiltering Examples:")
print("Engineers:\n", df[df['Department'] == 'Engineering'])
print("High earners:\n", df[df['Salary'] > 55000])
print("Missing ages:\n", df[df['Age'].isna()])

# Handling missing data
print("\nHandling Missing Data:")
print("Fill missing ages with mean:", df['Age'].fillna(df['Age'].mean()))
print("Drop rows with missing values:\n", df.dropna())

# Basic statistics
print("\nStatistical Summary:")
print("Mean salary:", df['Salary'].mean())
print("Age statistics:\n", df['Age'].describe())
print("Department counts:\n", df['Department'].value_counts())

# Adding new columns
df['Bonus'] = df['Salary'] * 0.1  # 10% bonus
df['Age Group'] = np.where(df['Age'] < 30, 'Young', 'Experienced')
print("\nDataFrame with new columns:\n", df)

# Grouping and aggregation
print("\nGrouping by Department:")
dept_stats = df.groupby('Department').agg({
    'Salary': ['mean', 'min', 'max'],
    'Age': 'mean'
})
print(dept_stats)
```

## 5. Usage Guidelines & Best Practices

*   **Import convention:** Always use `import pandas as pd`
*   **Method chaining:** Combine multiple operations in a single line for readability:
    ```python
    result = (df[df['Age'] > 25]
              .groupby('Department')
              ['Salary']
              .mean()
              .sort_values(ascending=False))
    ```
*   **Use vectorized operations:** Avoid iterating over rows with loops; use Pandas operations instead
*   **Copy warnings:** Be careful with the `inplace` parameter; it's often better to assign results to new variables
*   **Memory usage:** Use appropriate data types to reduce memory consumption

**Common Pitfalls:**
*   Using Python loops instead of vectorized Pandas operations
*   Confusing `loc[]` (label-based) and `iloc[]` (position-based) indexing
*   Modifying a DataFrame while iterating over it
*   Not handling missing data appropriately

## 6. Visual Aids

```
DataFrame Visualization:
      Name   Age  Salary  Department
0    Alice  25.0   50000  Engineering
1      Bob  30.0   60000       Sales
2  Charlie  35.0   70000  Engineering
3    Diana  28.0   55000    Marketing
4     Evan   NaN   48000       Sales

Series Visualization (Age column):
0    25.0
1    30.0
2    35.0
3    28.0
4     NaN
Name: Age, dtype: float64
```

## 7. Further Reading & Resources

*   **Pandas Official Documentation:** [Pandas User Guide](https://pandas.pydata.org/docs/user_guide/index.html)
*   **10 Minutes to Pandas:** [Quick Tutorial](https://pandas.pydata.org/docs/user_guide/10min.html)
*   **Real Python Pandas Tutorial:** [Pandas Tutorial](https://realpython.com/pandas-python-explore-dataset/)
*   **Pandas Exercises:** [Practice Problems](https://www.machinelearningplus.com/python/pandas-exercises/)

## 8. Summary & Key Takeaways

*   ✅ **Pandas** is the essential library for data manipulation in Python
*   ✅ **DataFrames** are 2D tabular structures (like Excel sheets)
*   ✅ **Series** are 1D labeled arrays (like DataFrame columns)
*   ✅ Pandas provides powerful tools for **data selection, filtering, and grouping**
*   ✅ Use **vectorized operations** instead of loops for better performance
*   ✅ Always handle **missing data** appropriately for your use case
*   ✅ The standard import is `import pandas as pd`

**➡️ Up Next:** In `1.2.1: Data Wrangling with Pandas`, you'll dive deeper into advanced data cleaning, transformation, and preparation techniques that are crucial for getting your data ready for AI models!

---

**🎯 Lab Exercises:**

1.  **DataFrame Creation:** Create a DataFrame with information about products (name, price, category)
2.  **Data Selection:** Practice selecting specific rows and columns from your DataFrame
3.  **Data Filtering:** Filter products based on price and category criteria
4.  **Data Aggregation:** Calculate average price by category

Example solution for exercise 4:
```python
import pandas as pd

# Create products DataFrame
products = pd.DataFrame({
    'name': ['Laptop', 'Mouse', 'Keyboard', 'Monitor', 'Tablet'],
    'price': [1200, 25, 80, 300, 600],
    'category': ['Electronics', 'Accessories', 'Accessories', 'Electronics', 'Electronics']
})

# Calculate average price by category
avg_price_by_category = products.groupby('category')['price'].mean()
print("Average price by category:")
print(avg_price_by_category)
```