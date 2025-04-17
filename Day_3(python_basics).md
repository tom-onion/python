# Day 3: User Input and Conditional Statements

Today, we'll make our programs more interactive by learning how to get input from the user. We'll also introduce the concept of conditional statements, which allow your program to make decisions based on certain conditions.

**Morning:**

1.  **Getting User Input:**
    * The `input()` function in Python is used to get input from the user.
    * When `input()` is called, the program pauses and waits for the user to type something and press Enter.
    * The `input()` function always returns the user's input as a **string**. You might need to convert it to other data types (like `int` or `float`) if you intend to perform numerical operations.
    * You can provide a prompt inside the parentheses of `input()` to display a message to the user before they enter their input.
    * Examples:
        ```python
        name = input("Enter your name: ")
        print("Hello, " + name + "!")

        age_str = input("Enter your age: ")
        age = int(age_str)  # Convert the input string to an integer
        print("You are", age, "years old.")

        height_str = input("Enter your height in meters: ")
        height = float(height_str) # Convert the input string to a float
        print("Your height is", height, "meters.")
        ```
    * **Important:** Always be mindful of potential `ValueError` if the user enters input that cannot be converted to the desired data type (e.g., entering text when expecting a number). We'll learn about error handling later.

**Afternoon:**

1.  **Conditional Statements (`if`, `elif`, `else`):**
    * Conditional statements allow your program to execute different blocks of code based on whether certain conditions are true or false.
    * **`if` statement:** Executes a block of code if a specified condition is true.
        ```python
        number = 10
        if number > 5:
            print("The number is greater than 5.")
        ```
    * **`else` statement:** Executes a block of code if the condition in the preceding `if` statement is false.
        ```python
        age = 15
        if age >= 18:
            print("You are eligible to vote.")
        else:
            print("You are not yet eligible to vote.")
        ```
    * **`elif` statement (else if):** Allows you to check multiple conditions in sequence. It is checked only if the preceding `if` (or `elif`) condition was false. You can have multiple `elif` statements.
        ```python
        grade = 85
        if grade >= 90:
            print("A")
        elif grade >= 80:
            print("B")
        elif grade >= 70:
            print("C")
        elif grade >= 60:
            print("D")
        else:
            print("F")
        ```
    * **Indentation is Crucial:** In Python, the blocks of code that belong to an `if`, `elif`, or `else` statement are defined by indentation (usually 4 spaces). Incorrect indentation will lead to errors.

2.  **Comparison Operators:**
    * Conditional statements typically involve comparing values using comparison operators:
        * `==`: Equal to (e.g., `x == y`)
        * `!=`: Not equal to (e.g., `x != y`)
        * `>`: Greater than (e.g., `x > y`)
        * `<`: Less than (e.g., `x < y`)
        * `>=`: Greater than or equal to (e.g., `x >= y`)
        * `<=`: Less than or equal to (e.g., `x <= y`)

3.  **Logical Operators:**
    * You can combine multiple conditions using logical operators:
        * `and`: Returns `True` if both conditions are true.
            ```python
            age = 25
            has_license = True
            if age >= 18 and has_license:
                print("You can drive.")
            else:
                print("You cannot drive.")
            ```
        * `or`: Returns `True` if at least one of the conditions is true.
            ```python
            is_weekend = True
            has_money = False
            if is_weekend or has_money:
                print("Let's go out!")
            else:
                print("Staying in.")
            ```
        * `not`: Negates a condition (returns `True` if the condition is false, and `False` if the condition is true).
            ```python
            is_raining = False
            if not is_raining:
                print("It's a sunny day!")
            else:
                print("Grab an umbrella.")
            ```

**Evening:**

1.  **Practice:**
    * Write programs that take user input and then use conditional statements to make decisions based on that input.
        * Example: Ask the user for a number and tell them if it's positive, negative, or zero.
        * Example: Ask the user for their age and check if they are a minor, young adult, or adult.
        * Example: Ask the user for two numbers and determine which one is larger (or if they are equal).
    * Experiment with combining multiple conditions using `and`, `or`, and `not`.
    * Pay close attention to indentation. Make sure the code blocks within your `if`, `elif`, and `else` statements are properly indented.
2.  **Further Exploration (Optional):**
    * Look into nested `if` statements (placing an `if` statement inside another `if` statement).
    * Consider how you might handle potential errors when converting user input (we'll cover more robust error handling later).

**Key Takeaways for Day 3:**

* You know how to use the `input()` function to get input from the user.
* You understand that `input()` returns a string and might need to be converted.
* You can use `if`, `elif`, and `else` statements to execute different code blocks based on conditions.
* You are familiar with comparison operators (`==`, `!=`, `>`, `<`, `>=`, `<=`).
* You can combine conditions using logical operators (`and`, `or`, `not`).
* Indentation is crucial for defining code blocks in conditional statements.

**Looking Ahead to [Day 4:](https://github.com/tom-onion/python/blob/main/Day_2(python_basics).md)**

Tomorrow, we will introduce the concept of loops (`for` and `while`) which allow you to repeat blocks of code multiple times. This will significantly expand the capabilities of your programs. Keep practicing!
