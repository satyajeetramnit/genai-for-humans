# `1.1.2: Controlling the Flow`

**Context & Relevance:** Now that you know how to create variables (the "nouns" of our program), it's time to make your code smarter. In this lesson, we'll learn about control flow - the "verbs" and "decision-making" parts of programming. This is how we tell the computer to make choices and repeat tasks, which is essential for handling the complex logic needed in AI.

## 1. Introduction & Overview

Right now, your code runs in a straight line from top to bottom. But what if you want your program to do different things based on different situations? Or repeat a task 100 times without writing the same line 100 times?

That's where **control flow** comes in. It allows your programs to branch out based on conditions and automate repetitive tasks. This is the foundation of creating intelligent behavior in code.

## 2. Basic Concepts & Definitions

*   **Conditional Statements (`if`, `elif`, `else`):** Code structures that allow your program to make decisions and execute different code blocks based on whether conditions are `True` or `False`.
    *   *Analogy:* Like choosing what to wear based on the weather. "IF it's raining, wear a jacket. ELSE, wear a t-shirt."
*   **Comparison Operators:** Tools to compare values (`==`, `!=`, `<`, `>`, `<=`, `>=`).
*   **Logical Operators:** Combine multiple conditions (`and`, `or`, `not`).
*   **Loops:** Structures that repeat code multiple times.
*   **`for` loop:** Repeats a block of code a specific number of times or for each item in a collection.
    *   *Analogy:* Like going through each student in a class to take attendance.
*   **`while` loop:** Repeats a block of code as long as a condition remains true.
    *   *Analogy:* Like keeping a door open WHILE someone is holding it.

## 3. Detailed Explanations

### Making Decisions with Conditionals

Life is full of choices, and so is programming. We use `if`, `elif` (else-if), and `else` statements to handle different scenarios:

```python
# Simple if statement
temperature = 25

if temperature > 30:
    print("It's hot outside!")
elif temperature > 20:
    print("It's a nice day!")
else:
    print("It's cold!")
```

The computer checks each condition in order and executes only the first block that matches.

### Repeating Tasks with Loops

Loops eliminate repetition and make your code more efficient:

**For Loop** - Perfect when you know how many times to repeat:
```python
# Count from 1 to 5
for number in range(1, 6):
    print(number)
```

**While Loop** - Great when you want to repeat until something changes:
```python
# Countdown from 5
count = 5
while count > 0:
    print(count)
    count -= 1  # Decrease count by 1
print("Blastoff!")
```

## 4. Practical Examples & Code Samples

Let's create a simple AI decision maker:

```python
# AI Assistant Decision Maker
weather = "rainy"
time_of_day = "morning"
has_umbrella = False

print("AI Assistant Recommendations:")
print("============================")

if weather == "rainy" and not has_umbrella:
    print("☔ Stay indoors or buy an umbrella!")
elif weather == "sunny":
    if time_of_day == "morning":
        print("🌞 Good morning! Perfect time for a walk.")
    else:
        print("😎 Great weather! Enjoy your day.")
else:
    print("🤔 Conditions are neutral. Carry on with your plans.")

# Loop through a list of tasks
print("\nYour agenda for today:")
tasks = ["Check emails", "AI project work", "Lunch break", "Meeting", "Exercise"]

for i, task in enumerate(tasks, 1):
    print(f"{i}. {task}")
```

## 5. Usage Guidelines & Best Practices

*   **Indentation Matters:** Python uses indentation (spaces) to show which code belongs to which block. Typically use 4 spaces.
*   **Clear Conditions:** Write conditions that are easy to read. Use parentheses to group complex conditions.
*   **Avoid Infinite Loops:** Always ensure your while loop has a way to eventually become False.
*   **Common Pitfalls:**
    *   Using `=` (assignment) instead of `==` (comparison) in conditions
    *   Forgetting the colon `:` at the end of conditionals and loops
    *   Not properly indenting code blocks

## 6. Visual Aids

```
Conditional Logic Flow:
Start → Check Condition → If True → Execute Block → Continue
               |
               ˅
          If False → Check Next Condition (elif) → If True → Execute Block → Continue
                               |
                               ˅
                          If All False → Execute Else Block → Continue

Loop Flow (while):
Start → Check Condition → If True → Execute Block → Check Condition Again...
               |
               ˅
          If False → Continue
```

## 7. Further Reading & Resources

*   **Python Official Docs:** [More on Control Flow](https://docs.python.org/3/tutorial/controlflow.html)
*   **Real Python:** [Conditional Statements](https://realpython.com/python-conditional-statements/)
*   **Interactive Practice:** [Python Loop Exercises](https://www.w3resource.com/python-exercises/python-conditional-statements-and-loop-exercises.php)

## 8. Summary & Key Takeaways

*   ✅ **Conditionals** (`if/elif/else`) let your programs make decisions based on conditions
*   ✅ **Comparison operators** (`==`, `!=`, `<`, `>`) compare values
*   ✅ **Logical operators** (`and`, `or`, `not`) combine multiple conditions
*   ✅ **For loops** iterate a specific number of times or over collections
*   ✅ **While loops** repeat as long as a condition remains true
*   ✅ **Proper indentation** is crucial for defining code blocks in Python

**➡️ Up Next:** In `1.1.3: Organizing Code with Functions`, you'll learn how to package your code into reusable blocks, making your programs more organized and efficient - essential for building complex AI systems!

---

**🎯 Lab Exercises:**

1.  **Weather Advisor:** Create a program that gives different advice based on temperature and weather conditions
2.  **Countdown Timer:** Build a countdown that asks the user for a number and counts down to zero
3.  **AI Shopping Cart:** Create a loop that lets users add items to a cart until they type "done", then show the total

Example solution for exercise 1:
```python
temperature = 15
is_raining = True

if temperature < 0:
    print("❄️ It's freezing! Stay warm and avoid travel.")
elif temperature < 10:
    if is_raining:
        print("🌧️ Cold and rainy - perfect indoor weather!")
    else:
        print("☁️ Chilly but dry - bundle up if going out.")
else:
    print("🌤️ Decent weather - enjoy your day!")
```