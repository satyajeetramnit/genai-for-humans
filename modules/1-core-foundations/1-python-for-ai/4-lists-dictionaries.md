# `1.1.4: Data Structures: Lists and Dictionaries`

**Context & Relevance:** Now that you understand functions and control flow, it's time to learn how to store and organize collections of data. In AI work, you'll rarely work with just single values - you'll handle datasets, model parameters, and complex information structures. Lists and dictionaries are the fundamental building blocks for organizing data in Python, making them essential for any AI practitioner.

## 1. Introduction & Overview

Imagine trying to manage a classroom of students without a roster, or a library without a catalog system. That's what programming would be like without data structures! Lists and dictionaries are Python's way of letting us store and organize multiple pieces of data together in a structured way.

In this lesson, you'll learn how to create, access, and manipulate these essential data structures. This knowledge forms the foundation for working with the complex datasets used in AI and machine learning.

## 2. Basic Concepts & Definitions

*   **List:** An ordered collection of items that can be changed (mutable). Items are stored in a specific order and accessed by their position (index).
    *   *Analogy:* Like a shopping list where items appear in a specific order, and you can add, remove, or change items.
*   **Dictionary:** An unordered collection of key-value pairs. Each item is accessed by a unique key rather than by position.
    *   *Analogy:* Like a real dictionary where you look up words (keys) to find their definitions (values).
*   **Index:** The position of an item in a list. In Python, indexing starts at 0.
*   **Key:** A unique identifier used to access a value in a dictionary.
*   **Value:** The data associated with a key in a dictionary.

## 3. Detailed Explanations

### Lists: Ordered Collections

Lists are perfect for storing sequences of items where order matters:

```python
# Creating a list
fruits = ["apple", "banana", "orange", "grape"]

# Accessing items by index (position)
print(fruits[0])  # Output: "apple" (first item)
print(fruits[2])  # Output: "orange" (third item)
print(fruits[-1]) # Output: "grape" (last item)

# Modifying lists
fruits.append("mango")     # Add to end
fruits.insert(1, "kiwi")   # Insert at specific position
fruits.remove("banana")    # Remove by value
fruits.pop(0)              # Remove by index

# Slicing: getting parts of a list
print(fruits[1:3])  # Items from index 1 to 2
print(fruits[:2])   # First two items
print(fruits[2:])   # From index 2 to end
```

### Dictionaries: Key-Value Pairs

Dictionaries are ideal for storing related information where each item has a unique identifier:

```python
# Creating a dictionary
person = {
    "name": "Alice",
    "age": 30,
    "occupation": "Data Scientist",
    "is_learning_ai": True
}

# Accessing values by key
print(person["name"])  # Output: "Alice"
print(person["age"])   # Output: 30

# Modifying dictionaries
person["age"] = 31              # Update existing value
person["city"] = "San Francisco" # Add new key-value pair
del person["occupation"]        # Remove a key-value pair

# Useful dictionary methods
print(person.keys())    # All keys
print(person.values())  # All values
print(person.items())   # All key-value pairs
```

## 4. Practical Examples & Code Samples

Let's see how these data structures are used in AI contexts:

```python
# Example 1: Storing and processing dataset features
house_features = ["bedrooms", "bathrooms", "square_footage", "year_built"]
house_data = [3, 2, 1500, 1995]

# Process each feature
for i in range(len(house_features)):
    print(f"{house_features[i]}: {house_data[i]}")

# Example 2: Storing model parameters with a dictionary
model_config = {
    "learning_rate": 0.01,
    "batch_size": 32,
    "hidden_layers": [64, 32, 16],
    "activation": "relu",
    "dropout_rate": 0.2
}

# Accessing model parameters
print(f"Learning rate: {model_config['learning_rate']}")
print(f"Hidden layers: {model_config['hidden_layers']}")

# Example 3: List of dictionaries for multiple data records
students = [
    {"name": "Alice", "score": 85, "passed": True},
    {"name": "Bob", "score": 62, "passed": False},
    {"name": "Charlie", "score": 91, "passed": True}
]

# Process student records
for student in students:
    status = "passed" if student["passed"] else "failed"
    print(f"{student['name']} {status} with score {student['score']}")
```

## 5. Usage Guidelines & Best Practices

*   **Choose the right structure:**
    *   Use lists when order matters or you have a collection of similar items
    *   Use dictionaries when you need to associate keys with values
*   **List comprehensions:** Create new lists concisely:
    ```python
    numbers = [1, 2, 3, 4, 5]
    squares = [x**2 for x in numbers]  # [1, 4, 9, 16, 25]
    ```
*   **Dictionary comprehensions:** Similarly for dictionaries:
    ```python
    numbers = [1, 2, 3, 4, 5]
    square_dict = {x: x**2 for x in numbers}  # {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
    ```
*   **Common Pitfalls:**
    *   Trying to access a list index that doesn't exist (IndexError)
    *   Trying to access a dictionary key that doesn't exist (KeyError)
    *   Modifying a list while iterating over it (can cause unexpected behavior)

## 6. Visual Aids

```
List Visualization:
Index:   0        1        2        3
Value: "apple" "banana" "orange" "grape"

Dictionary Visualization:
Key:    "name"    "age"    "occupation"
Value:  "Alice"    30      "Data Scientist"
```

## 7. Further Reading & Resources

*   **Python Official Docs:** [Data Structures](https://docs.python.org/3/tutorial/datastructures.html)
*   **Real Python:** [Lists and Tuples](https://realpython.com/python-lists-tuples/)
*   **Real Python:** [Dictionaries](https://realpython.com/python-dicts/)
*   **Interactive Practice:** [Data Structure Exercises](https://www.w3resource.com/python-exercises/data-structures-and-algorithms/)

## 8. Summary & Key Takeaways

*   ✅ **Lists** store ordered collections of items accessed by index
*   ✅ **Dictionaries** store unordered collections of key-value pairs
*   ✅ List indices start at 0 (not 1)
*   ✅ Dictionary keys must be unique and immutable (strings, numbers, or tuples)
*   ✅ Both lists and dictionaries are mutable (can be changed after creation)
*   ✅ Use list comprehensions and dictionary comprehensions for concise creation of these structures

**➡️ Up Next:** In `1.1.5: The World of Libraries: Intro to NumPy`, you'll learn about Python's powerful numerical computing library, which forms the foundation for nearly all AI and data science work!

---

**🎯 Lab Exercises:**

1.  **Shopping List Manager:** Create a program that lets users add, remove, and view items in a shopping list
2.  **Student Gradebook:** Create a dictionary that stores student names as keys and their grades as values, then calculate the class average
3.  **AI Training Data:** Create a list of dictionaries representing training examples with features and labels

Example solution for exercise 2:
```python
# Student gradebook
grades = {
    "Alice": 85,
    "Bob": 72,
    "Charlie": 91,
    "Diana": 68
}

# Add a new student
grades["Evan"] = 88

# Calculate class average
total = sum(grades.values())
average = total / len(grades)
print(f"Class average: {average:.2f}")

# Find students with grades above 80
high_achievers = [name for name, score in grades.items() if score > 80]
print(f"High achievers: {high_achievers}")
```