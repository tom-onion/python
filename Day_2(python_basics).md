# Day 2: Data Types and Basic Operations

Today, we'll build upon the foundation of Day 1 by exploring data types in more detail and learning how to perform basic arithmetic operations in Python.

**Morning:**

1.  **Review of Data Types:**
    * Briefly revisit the data types we encountered yesterday:
        * **String (`str`)**: Sequences of characters.
        * **Integer (`int`)**: Whole numbers.
        * **Float (`float`)**: Numbers with decimal points.
        * **Boolean (`bool`)**: `True` or `False`.
    * Understand that the data type of a variable determines the kind of operations you can perform on it.

2.  **String Operations:**
    * **Concatenation:** Joining strings together using the `+` operator.
        ```python
        greeting = "Hello"
        name = "World"
        message = greeting + ", " + name + "!"
        print(message)  # Output: Hello, World!
        ```
    * **String Repetition:** Repeating a string using the `*` operator.
        ```python
        star = "*"
        line = star * 5
        print(line)  # Output: *****
        ```
    * **String Indexing:** Accessing individual characters in a string using their index (position). Python uses zero-based indexing, meaning the first character is at index 0.
        ```python
        text = "Python"
        first_char = text[0]
        print(first_char)  # Output: P
        third_char = text[2]
        print(third_char)  # Output: t
        last_char = text[-1]  # Accessing from the end
        print(last_char)  # Output: n
        ```
    * **String Slicing:** Extracting a portion (substring) of a string using a range of indices. The syntax is `[start:end]`, where `start` is inclusive and `end` is exclusive.
        ```python
        language = "Programming"
        sub1 = language[0:4]  # Characters from index 0 up to (but not including) 4
        print(sub1)  # Output: Prog
        sub2 = language[4:]   # Characters from index 4 to the end
        print(sub2)  # Output: ramming
        sub3 = language[:7]   # Characters from the beginning up to (but not including) 7
        print(sub3)  # Output: Program
        sub4 = language[:]    # Creates a copy of the entire string
        print(sub4)  # Output: Programming
        ```

**Afternoon:**

1.  **Numeric Operations:**
    * **Arithmetic Operators:**
        * **Addition:** `+` (e.g., `5 + 3` results in `8`)
        * **Subtraction:** `-` (e.g., `10 - 4` results in `6`)
        * **Multiplication:** `*` (e.g., `2 * 6` results in `12`)
        * **Division:** `/` (e.g., `15 / 3` results in `5.0` - note that division always results in a float)
        * **Floor Division:** `//` (e.g., `15 // 3` results in `5`, `16 // 3` results in `5` - integer division, discards the remainder)
        * **Modulo (Remainder):** `%` (e.g., `16 % 3` results in `1` - gives the remainder of the division)
        * **Exponentiation:** `**` (e.g., `2 ** 3` results in `8` - 2 raised to the power of 3)
    * **Order of Operations (PEMDAS/BODMAS):** Python follows the standard order of operations: Parentheses/Brackets, Exponents/Orders, Multiplication and Division (from left to right), Addition and Subtraction (from left to right).
        ```python
        result1 = 10 + 5 * 2  # Multiplication happens before addition
        print(result1)       # Output: 20

        result2 = (10 + 5) * 2 # Parentheses change the order
        print(result2)       # Output: 30
        ```

2.  **Type Conversion (Casting):**
    * Sometimes, you need to convert a value from one data type to another. Python provides built-in functions for this:
        * `str()`: Converts a value to a string.
        * `int()`: Converts a value to an integer (if possible).
        * `float()`: Converts a value to a floating-point number (if possible).
        * `bool()`: Converts a value to a boolean.
    * **Important:** Not all conversions are possible and can lead to errors. For example, trying to convert the string "abc" to an integer will raise a `ValueError`.
    * Examples:
        ```python
        num_str = "123"
        num_int = int(num_str)
        print(num_int)       # Output: 123
        print(type(num_int)) # Output: <class 'int'>

        pi = 3.14159
        pi_str = str(pi)
        print(pi_str)       # Output: 3.14159
        print(type(pi_str)) # Output: <class 'str'>

        num_float = 5
        float_num = float(num_float)
        print(float_num)     # Output: 5.0
        print(type(float_num))# Output: <class 'float'>

        value1 = 0
        bool_value1 = bool(value1)
        print(bool_value1)   # Output: False

        value2 = "Hello"
        bool_value2 = bool(value2)
        print(bool_value2)   # Output: True
        ```

**Evening:**

1.  **Practice:**
    * Experiment with different string operations: concatenation, repetition, indexing, and slicing. Try to predict the output before running your code.
    * Perform various arithmetic operations using different numbers. Pay attention to the order of operations.
    * Try converting values between different data types using `str()`, `int()`, and `float()`. See what happens when you try to convert incompatible types.
    * Write small code snippets that combine string and numeric operations (e.g., create a string that includes the result of a calculation).
2.  **Further Exploration (Optional):**
    * Look up more advanced string methods in Python (e.g., `.upper()`, `.lower()`, `.find()`, `.replace()`). We'll cover these in more detail later, but it's good to be aware of them.
    * Research the concept of operator precedence in Python for a more in-depth understanding of how expressions are evaluated.

**Key Takeaways for Day 2:**

* You can manipulate strings using concatenation, repetition, indexing, and slicing.
* You can perform basic arithmetic operations in Python using operators like `+`, `-`, `*`, `/`, `//`, `%`, and `**`.
* Python follows the standard order of operations.
* You can convert values between different data types using `str()`, `int()`, and `float()`.

**Looking Ahead to [Day 3:](https://github.com/tom-onion/python/blob/main/Day_3(python_basics).md)**

Tomorrow, we will learn about how to take input from the user and introduce the fundamental concept of control flow using conditional statements (`if`, `elif`, `else`). Keep up the great work!
