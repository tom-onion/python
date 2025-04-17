# Day 4: Loops - `for` and `while`

Today, we'll learn about loops, which are fundamental control flow structures that allow you to execute a block of code repeatedly. Python offers two main types of loops: `for` loops and `while` loops.

**Morning:**

1.  **`for` Loops:**
    * `for` loops are primarily used to iterate over a sequence (like a list, tuple, string, or range) or other iterable objects. They execute a block of code for each item in the sequence.
    * **Syntax:**
        ```python
        for item in sequence:
            # Code to be executed for each item
        ```
    * **Iterating through a String:**
        ```python
        message = "Python"
        for char in message:
            print(char)
        ```
        Output:
        ```
        P
        y
        t
        h
        o
        n
        ```
    * **Iterating through a List:**
        ```python
        fruits = ["apple", "banana", "cherry"]
        for fruit in fruits:
            print(fruit)
        ```
        Output:
        ```
        apple
        banana
        cherry
        ```
    * **The `range()` function:** The `range()` function is often used with `for` loops to generate a sequence of numbers.
        * `range(stop)`: Generates numbers from 0 up to (but not including) `stop`.
        * `range(start, stop)`: Generates numbers from `start` up to (but not including) `stop`.
        * `range(start, stop, step)`: Generates numbers from `start` up to (but not including) `stop`, with a specified increment (`step`).
        ```python
        for i in range(5):  # Generates 0, 1, 2, 3, 4
            print(i)

        for j in range(2, 7): # Generates 2, 3, 4, 5, 6
            print(j)

        for k in range(0, 10, 2): # Generates 0, 2, 4, 6, 8
            print(k)
        ```

**Afternoon:**

1.  **`while` Loops:**
    * `while` loops execute a block of code as long as a specified condition is true.
    * **Syntax:**
        ```python
        while condition:
            # Code to be executed as long as the condition is true
            # It's important to have a way for the condition to eventually become false
            # to avoid an infinite loop.
        ```
    * **Example:** Counting down from 5
        ```python
        count = 5
        while count > 0:
            print(count)
            count = count - 1  # Decrement the counter
        print("Blast off!")
        ```
        Output:
        ```
        5
        4
        3
        2
        1
        Blast off!
        ```
    * **Infinite Loops:** If the condition in a `while` loop never becomes false, the loop will continue indefinitely. Be careful to ensure that your loop has a termination condition. You can often interrupt an infinite loop in most environments by pressing `Ctrl + C`.

2.  **`break` and `continue` Statements:**
    * These statements provide more control over the flow of loops.
    * **`break`:** Immediately terminates the loop and the program execution continues with the statement immediately following the loop.
        ```python
        numbers = [1, 2, 3, 4, 5]
        for num in numbers:
            if num == 3:
                break
            print(num)
        print("Loop finished.")
        ```
        Output:
        ```
        1
        2
        Loop finished.
        ```
    * **`continue`:** Skips the rest of the current iteration of the loop and proceeds to the next iteration.
        ```python
        numbers = [1, 2, 3, 4, 5]
        for num in numbers:
            if num == 3:
                continue
            print(num)
        ```
        Output:
        ```
        1
        2
        4
        5
        ```

3.  **`else` clause with Loops:**
    * Both `for` and `while` loops can have an optional `else` clause.
    * For a `for` loop, the `else` block is executed after the loop finishes iterating through all the items in the sequence (it is *not* executed if the loop is terminated by a `break` statement).
    * For a `while` loop, the `else` block is executed when the loop condition becomes false (it is *not* executed if the loop is terminated by a `break` statement).
        ```python
        for i in range(5):
            print(i)
        else:
            print("Loop completed successfully.")
        ```
        Output:
        ```
        0
        1
        2
        3
        4
        Loop completed successfully.
        ```

        ```python
        count = 0
        while count < 3:
            print(count)
            count += 1
        else:
            print("While loop condition is no longer true.")
        ```
        Output:
        ```
        0
        1
        2
        While loop condition is no longer true.
        ```

**Evening:**

1.  **Practice:**
    * Write `for` loops to:
        * Print the first 10 even numbers.
        * Calculate the sum of numbers in a list.
        * Iterate through a string and print each character in uppercase.
    * Write `while` loops to:
        * Simulate a countdown from a user-provided number.
        * Keep asking the user for input until they enter a specific word (e.g., "quit").
        * Calculate the factorial of a number.
    * Experiment with the `break` and `continue` statements within both `for` and `while` loops to see how they affect the loop's execution.
    * Try using the `else` clause with your loops.
2.  **Further Exploration (Optional):**
    * Look into nested loops (placing one loop inside another). Think about scenarios where this might be useful (e.g., iterating through a 2D grid).
    * Consider how you might use loops in conjunction with conditional statements to solve more complex problems.

**Key Takeaways for Day 4:**

* You understand how to use `for` loops to iterate over sequences.
* You know how to use the `range()` function to generate sequences of numbers for `for` loops.
* You understand how to use `while` loops to repeat a block of code as long as a condition is true.
* You are aware of the importance of having a termination condition in `while` loops to avoid infinite loops.
* You can use `break` to exit a loop prematurely and `continue` to skip the current iteration.
* You understand the optional `else` clause in loops and when it is executed.

**Looking Ahead to [Day 5:](https://github.com/python/Day_5(python_basics).md)**

Tomorrow, we will introduce data structures like lists and tuples, which are essential for organizing and managing collections of data. You'll see how loops become even more powerful when working with these structures. Keep up the excellent progress!