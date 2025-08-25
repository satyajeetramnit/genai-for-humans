# `1.1.1: Python Basics - Your First Steps`

**Context & Relevance:** Welcome to the very first step of your GenAI journey! This subtopic is the foundation of everything that follows. Just like you need to learn the alphabet before you can write a novel, you need to understand these Python basics before you can build intelligent systems. Don't worry—we'll take it slow and make it fun.

## 1. Introduction & Overview

So, you want to talk to computers and tell them what to do? Awesome! To do that, we need to learn a language they understand. In the world of AI, that language is most often **Python**.

Think of Python like a super-powerful calculator that can also work with words, data, and eventually, artificial brains. In this guide, we'll learn the basic "words" and "grammar" of Python to write our first simple instructions, or "scripts."

## 2. Basic Concepts & Definitions

Let's break down the absolute essentials:

*   **Python:** A programming language known for being readable and beginner-friendly. It's the go-to tool for AI, data science, and web development.
*   **Variable:** A named container that stores a piece of information. It's like a labeled box. You can put something in it, look inside it, or replace what's inside.
    *   *Analogy:* Think of a variable like a name tag. You can put a name tag on a person (value) and then refer to that person by their tag (variable name).
*   **Data Type:** The kind of information a variable holds. The basic types are:
    *   `int`: A whole number (e.g., `5`, `-10`, `1000`)
    *   `float`: A decimal number (e.g., `3.14`, `-0.5`, `2.0`)
    *   `str` (String): Text. Always wrapped in quotes (e.g., `"hello"`, `'AI'`, `"42"`)
    *   `bool` (Boolean): A simple `True` or `False` value.

## 3. Detailed Explanations

### How It Works (Plain Language)
We write instructions in a file (a **script**) and then tell the computer to run that file. The computer reads it from top to bottom and does exactly what we say. Our goal is to give it clear, correct instructions.

### How It Works (Slightly More Technical)
When you run a Python script, the **Python Interpreter** reads your code, translates it into machine code (1s and 0s) that the computer's CPU understands, and executes it.

### Real-World Scenario
Imagine you're writing a recipe. The recipe is your script. The ingredients (`"flour"`, `3`, `"eggs"`) are your data. The instructions ("mix for 5 minutes") are your code. You (the interpreter) follow the recipe step-by-step to create the final dish (the program output).

## 4. Practical Examples & Code Samples

Let's open a code editor (like VS Code) or a notebook (like Google Colab) and try this.

```python
# This is a comment. It doesn't do anything. It's for us humans to read.

# Let's create some variables (our labeled boxes)
name = "Alice"  # A string (text)
age = 30        # An integer (whole number)
temperature = 98.6 # A float (decimal number)
is_learning = True # A boolean (True or False)

# Now, let's print what's inside our boxes to the screen
print("Hello, world!") # Prints the text directly
print(name)            # Prints the value inside the 'name' variable
print("Age:", age)     # Combines text and a variable
print("Is learning:", is_learning)
```

**Try it yourself!** Type this code into your editor and run it. You should see:
```
Hello, world!
Alice
Age: 30
Is learning: True
```

## 5. Usage Guidelines & Best Practices

*   **Clear Names:** Use descriptive names for variables. `user_name` is better than `x`.
*   **The `print()` Function:** Your best friend for seeing what's happening. When in doubt, `print()` it out!
*   **Common Pitfalls:**
    *   **Forgetting Quotes:** `name = Alice` (Error!) vs. `name = "Alice"` (Correct!).
    *   **Spelling Matters:** `Name` and `name` are two different variables. Computers are very literal.

## 6. Visual Aids

Here’s how variables work:
```
+---------+      +-------+
|  name   | ---> |"Alice"|
+---------+      +-------+

+---------+      +-----+
|   age   | ---> | 30  |
+---------+      +-----+
```
The variable name *points* to the value stored in the computer's memory.

## 7. Further Reading & Resources

*   **Official Python Tutorial:** [The Python Tutorial](https://docs.python.org/3/tutorial/)
*   **Google's Python Class:** [Google for Education](https://developers.google.com/edu/python)

## 8. Summary & Key Takeaways

*   ✅ **Variables** are named containers that store information.
*   ✅ The basic **data types** are `int`, `float`, `str`, and `bool`.
*   ✅ Use the **`print()`** function to display information.
*   ✅ Code is executed **line by line** from top to bottom.

**➡️ Up Next:** In `1.1.2: Controlling the Flow`, we'll learn how to make your programs make decisions (`if` statements) and repeat tasks (`for` loops), making them much more powerful!

---

**🎯 Lab Exercise:** 
1.  Create variables for a character in a story: their name, job, and health points.
2.  Print out a sentence that uses all of these variables. 
Example output: `"Meet Alice the warrior, they have 100 health points."`