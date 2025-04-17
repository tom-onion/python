# Day 7: Functions

Today, we'll learn about **functions**, which are fundamental building blocks for creating organized and reusable code in Python. Functions allow you to encapsulate a block of code that performs a specific task, and you can call this function whenever you need to execute that task.

**Morning:**

1.  **Introduction to Functions:**
    * A function is a block of organized, reusable code that performs a single, related action.
    * Functions help to break down larger programs into smaller, more manageable and modular pieces.
    * They promote code reusability, making your code more efficient and easier to understand and maintain.
    * In Python, you define a function using the `def` keyword, followed by the function name, parentheses `()`, and a colon `:`. The code block within the function is indented.
    * **Syntax:**
        ```python
        def function_name(parameters):
            """Optional docstring to describe what the function does"""
            # Code to be executed within the function
            # Optional return statement
        ```
    * **Function Definition:** This is where you create the function and specify its name, parameters (inputs), and the code it will execute.
    * **Function Call:** To execute the code inside a function, you need to "call" the function by its name followed by parentheses `()`. If the function expects arguments (parameters), you provide them within the parentheses during the call.

2.  **Defining and Calling Simple Functions:**
    * **Function with no parameters and no return value:**
        ```python
        def greet():
            print("Hello!")

        greet()  # Calling the function
        ```
        Output:
        ```
        Hello!
        ```
    * **Function with parameters:**
        ```python
        def greet_user(name):
            print(f"Hello, {name}!")

        greet_user("Bob")   # Calling the function with an argument
        greet_user("Charlie")
        ```
        Output:
        ```
        Hello, Bob!
        Hello, Charlie!
        ```

3.  **Return Values:**
    * Functions can optionally return a value back to the caller using the `return` statement.
    * When a `return` statement is executed, the function's execution stops, and the specified value is returned.
    * If a function does not have a `return` statement, or if the `return` statement is used without a value (`return`), the function implicitly returns `None`.
    * **Function with a return value:**
        ```python
        def add(x, y):
            sum_result = x + y
            return sum_result

        result = add(5, 3)
        print(result)  # Output: 8
        ```
    * **Returning multiple values (as a tuple):**
        ```python
        def get_name_and_age():
            name = "David"
            age = 30
            return name, age

        person_info = get_name_and_age()
        print(person_info)      # Output: ('David', 30)
        name, age = get_name_and_age() # Unpacking the returned tuple
        print(f"Name: {name}, Age: {age}") # Output: Name: David, Age: 30
        ```

**Afternoon:**

1.  **Function Parameters:**
    * **Positional Arguments:** Arguments are passed to the function based on their position in the function call. The order matters.
        ```python
        def describe_pet(animal_type, pet_name):
            print(f"I have a {animal_type} named {pet_name}.")

        describe_pet("dog", "Lucy")   # animal_type = "dog", pet_name = "Lucy"
        describe_pet("Lucy", "dog")   # animal_type = "Lucy", pet_name = "dog" (order matters!)
        ```
    * **Keyword Arguments:** You can pass arguments using the parameter names as keywords. This allows you to pass arguments in any order, and it makes the function call more readable.
        ```python
        def describe_pet(animal_type, pet_name):
            print(f"I have a {animal_type} named {pet_name}.")

        describe_pet(animal_type="cat", pet_name="Whiskers")
        describe_pet(pet_name="Buddy", animal_type="golden retriever")
        ```
    * **Default Parameter Values:** You can specify default values for parameters in the function definition. If an argument for that parameter is not provided in the function call, the default value is used.
        ```python
        def power(base, exponent=2):  # exponent has a default value of 2
            result = base ** exponent
            return result

        print(power(5))       # Uses the default exponent (5^2 = 25)
        print(power(3, 4))    # Overrides the default exponent (3^4 = 81)
        ```
    * **Arbitrary Arguments (`*args`):** If you don't know in advance how many arguments a function will receive, you can use `*args`. This collects any extra positional arguments into a tuple.
        ```python
        def sum_all(*args):
            total = 0
            for num in args:
                total += num
            return total

        print(sum_all(1, 2))       # Output: 3
        print(sum_all(1, 2, 3, 4)) # Output: 10
        ```
    * **Arbitrary Keyword Arguments (`**kwargs`):** Similarly, `**kwargs` allows a function to accept an arbitrary number of keyword arguments. These are collected into a dictionary.
        ```python
        def build_profile(first, last, **kwargs):
            profile = {'first_name': first, 'last_name': last}
            profile.update(kwargs)
            return profile

        user_profile = build_profile("albert", "einstein", location="princeton", field="physics")
        print(user_profile)
        # Output: {'first_name': 'albert', 'last_name': 'einstein', 'location': 'princeton', 'field': 'physics'}
        ```

2.  **Docstrings:**
    * A docstring (documentation string) is a multiline string used to document what a function does, its parameters, and what it returns.
    * It's good practice to include docstrings for all your functions to make them more understandable.
    * Docstrings are enclosed in triple quotes (`"""Docstring goes here"""`).
    * You can access a function's docstring using the `__doc__` attribute.
        ```python
        def square(n):
            """Return the square of a number n."""
            return n ** 2

        print(square(5))
        print(square.__doc__)  # Output: Return the square of a number n.
        ```

**Evening:**

1.  **Practice:**
    * Write functions to perform various tasks you've learned so far (e.g., calculate the factorial of a number, check if a number is prime, reverse a string).
    * Experiment with different types of function parameters (positional, keyword, default, `*args`, `**kwargs`).
    * Write functions that return single and multiple values.
    * Make sure to include clear and concise docstrings for all your functions.
    * Call your functions with different arguments to test their behavior.
2.  **Further Exploration (Optional):**
    * Look into the concept of function scope (local vs. global variables).
    * Research lambda functions (anonymous functions) in Python, which are small, single-expression functions.

**Key Takeaways for Day 7:**

* You understand the purpose and benefits of using functions in Python.
* You know how to define and call functions with and without parameters.
* You can use the `return` statement to return values from functions.
* You are familiar with different types of function parameters: positional, keyword, default, arbitrary positional (`*args`), and arbitrary keyword (`**kwargs`).
* You understand the importance of docstrings for documenting your functions.

**Looking Ahead to [Day 8:](https://github.com/python/Day_8(python_basics).md)**

Tomorrow, we will delve into **modules and packages**. Modules allow you to organize your Python code into separate files, and packages provide a way to structure these modules into a hierarchy. This is crucial for building larger and more complex projects. Keep practicing writing functions!