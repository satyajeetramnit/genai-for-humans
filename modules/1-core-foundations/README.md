### **Module 1: Core AI Foundations**

#### **1. Overall Purpose & "The Why"**
This module is the **boot camp**. Its sole job is to take someone from little or no programming/ML experience and equip them with the non-negotiable, practical skills needed to not just follow along with GenAI code, but to understand *why* things work the way they do. It answers the question: "What do I need to learn *before* I can learn about LLMs?"

#### **2. Learning Objectives**
By the end of Module 1, a learner should be able to:
*   Write basic Python scripts to manipulate data and automate tasks.
*   Use NumPy for efficient numerical computations.
*   Use Pandas to load, clean, explore, and analyze tabular data.
*   Write basic SQL queries to retrieve and aggregate data from a database.
*   Explain the core concepts of machine learning: models, training, inference, and evaluation.
*   Build, train, and evaluate a simple machine learning model using scikit-learn.
*   Articulate the intuition behind core mathematical concepts (vectors, gradients, probability) without getting bogged down by advanced notation.

#### **3. Detailed Subtopic Breakdown**

Here is a granular list of subtopics for Module 1. Each of these would become its own `README.md` file within the `modules/1-core-foundations/` directory.

**Topic 1.1: Python for AI**
*   **1.1.1: Python Basics: Your First Steps**
    *   Context: Why Python? Setting up the dev environment (VS Code/PyCharm/Colab).
    *   Content: Variables, data types (`int`, `float`, `str`, `bool`), basic operators, and printing.
    *   Lab: Write a script that converts temperatures from Fahrenheit to Celsius.
*   **1.1.2: Controlling the Flow**
    *   Context: Programs need to make decisions and repeat tasks.
    *   Content: Conditional logic (`if`, `elif`, `else`), `for`-loops, `while`-loops.
    *   Lab: Create a number guessing game.
*   **1.1.3: Organizing Code with Functions**
    *   Context: Avoiding repetition and making code readable and reusable.
    *   Content: Defining functions, parameters, return statements, scope.
    *   Lab: Refactor the labs from 1.1.1 and 1.1.2 into functions.
*   **1.1.4: Data Structures: Lists and Dictionaries**
    *   Context: How to store collections of data.
    *   Content: Lists (indexing, slicing, methods), Dictionaries (key-value pairs).
    *   Lab: Create a simple customer database using a list of dictionaries.
*   **1.1.5: The World of Libraries: Intro to NumPy**
    *   Context: Pure Python is slow for math. NumPy is fast because it works on arrays.
    *   Content: Creating arrays, array shapes, broadcasting, universal functions.
    *   Lab: Perform mathematical operations on arrays of data.
*   **1.1.6: The AI Data Wrangler: Intro to Pandas**
    *   Context: NumPy is for numbers. Pandas is for labeled, table-like data (the most common data format).
    *   Content: Series and DataFrames, reading CSVs, viewing data, selecting columns/rows.
    *   Lab: Load a dataset (e.g., iris, titanic) and explore its basic properties.

**Topic 1.2: Data Wrangling & SQL**
*   **1.2.1: Taming Data with Pandas**
    *   Context: Real-world data is messy.
    *   Content: Handling missing values, filtering data, creating new columns.
    *   Lab: Clean a messy dataset.
*   **1.2.2: Talking to Databases: SQL Basics**
    *   Context: Data doesn't live in CSVs in real companies; it lives in databases.
    *   Content: What is a relational database? The `SELECT` statement, `FROM`, `WHERE`.
    *   Lab: Query a SQLite database to find specific records.
*   **1.2.3: Asking Deeper Questions with SQL**
    *   Context: We need to summarize and aggregate data, not just look at rows.
    *   Content: `GROUP BY`, `ORDER BY`, `COUNT`, `SUM`, `AVG`, `JOIN` (simple INNER JOIN).
    *   Lab: Write queries to generate reports from a database (e.g., "total sales per region").

**Topic 1.3: Math for AI (Simplified)**
*   **1.3.1: Vectors & Matrices: The Language of AI**
    *   Context: Everything in AI (text, images) gets turned into lists of numbers (vectors).
    *   Content: Vectors as points in space, matrices as transformations. Dot products. (All explained with NumPy).
    *   Lab: Calculate word similarities using simple vector operations.
*   **1.3.2: Calculus Intuition: The Engine of Learning**
    *   Context: How do models actually *learn* from error?
    *   Content: The concept of a derivative as slope. The gradient as the direction of steepest ascent. Intuition behind gradient descent. **No complex formulas.**
    *   Lab: Implement a simple gradient descent to find the minimum of a function.
*   **1.3.3: Probability Intuition: Dealing with Uncertainty**
    *   Context: AI deals in predictions, which are never 100% certain.
    *   Content: Probability distributions (Normal). Basic rules. Bayes' Theorem intuition.
    *   Lab: Simulate a coin flip to demonstrate probability.

**Topic 1.4: ML Fundamentals**
*   **1.4.1: What is Machine Learning?**
    *   Context: Defining the core paradigm shift from traditional programming.
    *   Content: Supervised vs. Unsupervised Learning. The concepts of "Features" and "Labels".
    *   Lab: N/A (Conceptual).
*   **1.4.2: Your First Model: Linear Regression**
    *   Context: The "Hello, World!" of ML. Predicting a continuous number.
    *   Content: The scikit-learn API: `fit()`, `predict()`. Evaluating with Mean Squared Error.
    *   Lab: Predict house prices based on square footage.
*   **1.4.3: Classifying Things: Logistic Regression**
    *   Context: Predicting categories (spam/not spam, cat/dog).
    *   Content: Classification vs. Regression. Evaluation with accuracy.
    *   Lab: Build a classifier to predict iris flower species.
*   **1.4.4: The Cardinal Sin: Overfitting**
    *   Context: Why a model that works perfectly on your data might fail in the real world.
    *   Content: The concept of memorizing vs. learning. Train/Test split.
    *   Lab: Demonstrate overfitting by showing perfect training accuracy but poor test accuracy.

---